Keystore Configuration

https://www.baeldung.com/java-https-client-certificate-authentication

Remote Delivery

https://james.apache.org/server/3/apidocs/org/apache/james/transport/mailets/RemoteDelivery.html

mail.smtp.ssl.*

https://javaee.github.io/javamail/docs/api/com/sun/mail/smtp/package-summary.html

Java mail send over ssl

https://www.javacodegeeks.com/2020/02/java-mail-sent-over-ssl.html

https://github.com/mjremijan/thoth-email/blob/master/thoth-email-via-ssl/src/test/java/org/thoth/email/via/ssl/SslTest.java

```
      props.setProperty("mail.smtp.auth", "true");
      props.setProperty("mail.smtp.host", yahoo.getProperty("host"));
      props.setProperty("mail.smtp.socketFactory.port", yahoo.getProperty("port"));
      props.setProperty("mail.smtp.socketFactory.class", "javax.net.ssl.SSLSocketFactory");
```

https://learn.microsoft.com/en-us/answers/questions/381623/javaxmailmessagingexception-could-not-convert-sock.html

```
Properties props = new Properties();
 props.put("mail.smtp.socketFactory.fallback", "false");  
 props.put("mail.smtp.quitwait", "false");
 props.put("mail.smtp.socketFactory.port", "587");  
 props.put("mail.host", smtp.office365.com);
    
 props.setProperty("mail.transport.protocol", "smtp");
    
 props.setProperty("mail.smtp.port", "587");
 props.setProperty("mail.smtp.ssl.trust", "*");
 props.setProperty("mail.smtp.starttls.enable", String.valueOf(requireTls));//True or False
 props.setProperty("mail.smtp.ssl.protocols", "TLSv1.2");
 props.setProperty("mail.smtp.timeout", "300000");
 props.setProperty("mail.smtp.connectiontimeout", "300000");
 props.setProperty("mail.smtp.writetimeout", "300000");
```
