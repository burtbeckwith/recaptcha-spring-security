recaptcha-spring-security
=========================

Grails: Using recaptcha with spring security core for brute force defender

based in: [Brute Force Defender](https://github.com/grygoriy/bruteforcedefender)

Requirements
========================

1. Grails 1.3.7+
2. [Spring Security Core Plugin](http://grails.org/plugin/spring-security-core) (1.2.7.3+)
3. [ReCaptcha Plugin](http://grails.org/plugin/recaptcha) (0.5.3+)

Installation
========================

1. clone the repository: git clone https://github.com/rpalcolea/recaptcha-spring-security.git

2. Enter to the repository via command line.

3. package the plugin: grails package-plugin

Configuration
========================

## Config.groovy

Add the following lines to your Grails Config.groovy file:

	bruteforcedefender {
    	time = 5
    	allowedNumberOfAttempts = 3
	}

time = minutes mantaining failed attempts
allowedNumberOfAttempts = number of failed attempts before showing the recaptcha widget.

Adding the recaptcha to your auth view
======================== 

Open your auth.gsp (/grails-app/views/login/auth.gsp) and add the next line wherever you want to render the recaptcha after the attempts.

          <g:recaptchaLogin/>


Extras
========================

Thanks to [Vinco Orbis](http://www.vincoorbis.com)