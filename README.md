# springboot-study

# 注意：

出现javax.mail.AuthenticationFailedException: 535 Error: ÇëÊ¹ÓÃÊÚÈ¨ÂëµÇÂ¼¡£ÏêÇéÇë¿´是因为密码需要填写的时qq邮箱的授权码。授权码可以在邮箱 ==> 设置  ==> 账户。开启pop3，然后通过短信验证获取授权码。

java mail发邮件是附件名过长默认会被截断显示乱码，在程序启动时设置主动设置为false可正常显示，具体设置代码如下:
        
        //java mail发邮件时附件名过长默认会被截断，附件名显示【tcmime.29121.29517.50430.bin】，主动设为false可正常显示附件名
            System.setProperty("mail.mime.splitlongparameters", "false");
            SpringApplication.run(SendMailApplication.class, args);
        }