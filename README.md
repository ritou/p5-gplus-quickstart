# p5-gplus-quickstart

This quick-start app is built in Perl and lets you get started with the Google+ platform in a few minutes.

* [Sign-In flow using plusone.js and server-side library](https://developers.google.com/+/web/signin/server-side-flow?hl=ja#using_one-time-code_flow)
* [Sign-In flow using server-side library only](https://developers.google.com/accounts/docs/OAuth2Login?hl=ja)

## Step 1: Enable the Google+ API

Create a Google Developers Console project, OAuth 2.0 client ID, and register your JavaScript origins:

1. Go to the [Google Developers Console](https://console.developers.google.com/project).  
2. Select a project, or create a new one.  
3. In the sidebar on the left, select APIs & auth. APIs is automatically selected.  
4. In the displayed list of APIs, find the Google+ API service and set its status to ON.  
5. In the sidebar on the left, select Credentials.  
6. In the OAuth section of the page, select Create New Client ID.  

In the resulting Create Client ID dialog box, register the origins where your app is allowed to access the Google APIs. The origin is the unique combination of protocol, hostname, and port.

* In the Application type section of the dialog, select Web application.  
* In the Authorized JavaScript origins field, enter the origin for your app. You can enter multiple origins to allow for your app to run on different protocols, domains, or subdomains. Wildcards are not allowed. In the example below, the second URL could be a production URL.

    http://localhost:4567  
    http://myproductionurl.example.com


Select Create Client ID.  
In the resulting Client ID for web application section, note or copy the Client ID and Client secret that your app will need to use to access the APIs.

## Step 2: Set up the Perl quick-start app

0. Setup perl and carton environment  
[xbuild](https://github.com/tagomoris/xbuild) is very useful.
1. Get the latest version of the quick-start. One way is to use git to clone the application repository.

    $ git clone https://github.com/ritou/p5-gplus-quickstart.git
    $ cd p5-gplus-quickstart

3. Install libraries

    $ carton install

4. Modify configuration for your client credentials

    $ cp app.psgi.sample app.psgi
    $ vim app.psgi

## step 3: Run the application

1. Run psgi app

    $ carton exec -- plackup -p (your app's port number)

2. Access your application

    http://(your app's hostname):(your app's port number)


