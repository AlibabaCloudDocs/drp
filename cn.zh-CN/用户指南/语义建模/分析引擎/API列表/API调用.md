# API调用

本章节为您介绍如何调用API。

发布API成功。

API调用代码支持java和node.js。

1.  登录[数据资源平台控制台](https://dataq.console.aliyun.com)。

2.  在菜单栏左上角，单击**![菜单](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/6504337061/p188771.png)**按钮，选择**研发工作台**。

3.  单击**资产加工** \> **![语义建模](https://static-aliyun-doc.oss-accelerate.aliyuncs.com/assets/img/zh-CN/1290330161/p208848.png)** \> **分析引擎** \> **API列表**。

4.  单击API后的**详情**，查看API调用示例代码。

    -   Java格式示例代码：

        ```
        
        package com.aliyun.dataq.jdbc.proxy;
        
        import java.io.BufferedReader;
        import java.io.IOException;
        import java.io.InputStreamReader;
        import java.io.PrintWriter;
        import java.net.HttpURLConnection;
        import java.net.MalformedURLException;
        import java.net.URL;
        import java.security.MessageDigest;
        import java.text.SimpleDateFormat;
        import java.util.Date;
        import java.util.Locale;
        import javax.crypto.Mac;
        import javax.crypto.spec.SecretKeySpec;
        
        import sun.misc.BASE64Encoder;
        
        public class Main {
        
           public static void main(String[] args) throws Exception {
               // ak信息
               String akId = "R0FdoDWLh0oKT92y";
               String akSecret = "9f1EXyWnKtXomhANk82lO5M5zdAbGzIu";
        
               // 需要请求的接口
               String url = "http://daily.dtboost.biz.aliyun.test/analysis/api/service/search?workspaceCode=profile";
               String body = "{\"params\":{\"age\": \"20\"}}";  // 参数为 json
               String method = "POST";
               String gmtDate = toGMTString(new Date());
               // 生成签名,签名需要放在header里 重要 ！！！！！
               String signature = generateSignature(method, akId, akSecret, url, body, gmtDate);
        
               // 创建http连接
               URL realUrl = new URL(url);
               HttpURLConnection conn = (HttpURLConnection) 
               realUrl.openConnection();
        
               // 设置信息校验的头部，重要 ！！！！
               conn.setRequestMethod(method);
               // 设置租户信息 必填
               conn.setRequestProperty("X-Access-TenantCode", "profile");
               // accept 必填
               conn.setRequestProperty("accept", "json");
               // contentType 必填
               conn.setRequestProperty("content-type", "application/json");
               // 日期 必填
               conn.setRequestProperty("date", gmtDate);
               // 签名 必填
               conn.setRequestProperty("Authorization", signature);
               // body体 md5 post/put必填（ get请求不用填 ）
               conn.setRequestProperty("Content-MD5", MD5Base64(body));
               conn.setDoOutput(true);
               conn.setDoInput(true);
        
               // 获得返回结果
               String result = getResult(body, method, conn);
               System.out.println("response body:" + result);
            }
        
           private static String getResult(String body, String method, HttpURLConnection conn) throws IOException {
               PrintWriter out = new PrintWriter(conn.getOutputStream());
               BufferedReader in = null;
               String result = "";
               try {
                  out.print(body);
                  out.flush();
        
                  if (conn.getResponseCode() != 200) {
                      in = new BufferedReader(new InputStreamReader(conn.getErrorStream()));
                  } else {
                      in = new BufferedReader(new InputStreamReader(conn.getInputStream()));
                  }
                  String line;
                  while ((line = in.readLine()) != null) {
                      result += line;
                  }
               } catch (Exception e) {
                   System.out.println(" " + method + " " + e);
                   e.printStackTrace();
               } finally {
                   try {
                       if (out != null) {
                          out.close();
                       }
                       if (in != null) {
                          in.close();
                       }
                   } catch (IOException ex) {
                       ex.printStackTrace();
                   }
               }
               return result;
            }
        
           private static String generateSignature(String method, String ak_id, String ak_secret, String url, String body, String gmtDate) throws MalformedURLException {
               URL realUrl = new URL(url);
               String accept = "json";
               String content_type = "application/json";
               String path = realUrl.getFile();
               String date = gmtDate;
               String bodyMd5 = MD5Base64(body);
               String stringToSign = "";
               if (method.equals("GET")) {
                 stringToSign = method + "\n" + accept + "\n" + content_type + "\n" + date + "\n" + path;
                }else {
                   stringToSign = method + "\n" + accept + "\n" + bodyMd5 + "\n" + content_type + "\n" + date + "\n" + path;
               }
               String signature = HMACSha1(stringToSign, ak_secret);
               return "dtboost-proxy " + ak_id + ":" + signature;
            }
        
           public static String MD5Base64(String s) {
               if (s == null)
                  return null;
               String encodeStr = "";
               byte[] utfBytes = s.getBytes();
               MessageDigest mdTemp;
               try {
                   mdTemp = MessageDigest.getInstance("MD5");
                   mdTemp.update(utfBytes);
                   byte[] md5Bytes = mdTemp.digest();
                   BASE64Encoder b64Encoder = new BASE64Encoder();
                   encodeStr = b64Encoder.encode(md5Bytes);
                } catch (Exception e) {
                   throw new Error("Failed to generate MD5 : " + e.getMessage());
                }
               return encodeStr;
           }
        
           public static String HMACSha1(String data, String key) {
                String result;
                try {
                   SecretKeySpec signingKey = new SecretKeySpec(key.getBytes(),"HmacSHA1");
                   Mac mac = Mac.getInstance("HmacSHA1");
                   mac.init(signingKey);
                   byte[] rawHmac = mac.doFinal(data.getBytes());
                   result = (new BASE64Encoder()).encode(rawHmac);
               } catch (Exception e) {
                   throw new Error("Failed to generate HMAC : " + e.getMessage());
               }
               return result;
            }
        
           public static String toGMTString(Date date) {
               SimpleDateFormat df = new SimpleDateFormat("E, dd MMM yyyy HH:mm:ss z",Locale.UK);
               df.setTimeZone(new java.util.SimpleTimeZone(0, "GMT"));
               return df.format(date);
           }
        }
                                    
        ```

    -   node.js调用代码：

        ```
        
        const request = require('request');
        const url = require('url');
        const crypto = require('crypto');
        // 请到右上角 用户配置 中获取你拿的ak，请注意防止泄露
        const ak_id = '';
        const ak_secret = '';
        const options = {
          url: 'https://dtplus-dataq-cloud.data.aliyuncs.com/tenant_1619191348122093/porana/analysis/api/service/api_path_OR87RL12N?workspaceCode=default_group',
          method: 'POST',
          body: JSON.stringify({
            params:{
        
            }
          }),
          headers: {
            'accept': 'json',
            'content-type': 'application/json',
            'date': new Date().toUTCString(),
            'Authorization': '',
            'x-access-tenantCode': 'tenant_1619191348122093'
          }
        };
        const md5 = function (buffer) {
          return crypto.createHash('md5').update(buffer).digest('base64');
        };
        const sha1 = function (stringToSign, secret) {
          return crypto.createHmac('sha1', secret).update(stringToSign).digest().toString('base64');
        };
        let body = options.body || '';
        let bodymd5;
        if (options.method === 'GET' || body === void 0 || body === '') {
          bodymd5 = body;
        } else {
          bodymd5 = md5(Buffer.from(body));
        }
        let stringToSign = options.method + "\n" + options.headers.accept + "\n" + bodymd5 +
          "\n" + options.headers['content-type'] + "\n" + options.headers.date + "\n" +
          url.parse(options.url).path;
        let signature = sha1(stringToSign, ak_secret);
        let authHeader = "dtoobst-proxy " + ak_id + ":" + signature;
        options.headers.Authorization = authHeader;
        
        function callback(error, response, body) {
          if (error) {
            console.error("error", error)
          }
          console.log("result: ", response.statusCode, body)
        }
        request(options, callback);
        
                                    
        ```


