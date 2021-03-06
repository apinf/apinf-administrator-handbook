# Configuration

You can configure Apinf branding and other settings after registering an initial **admin** account. **Note:** The first registered user will become Admin.

1. Signup to the APInf [http://YOUR\_SITE\_DOMAIN/sign-up](http://YOUR_SITE_DOMAIN/sign-up)
2. Login to the APInf web admin [http://YOUR\_SITE\_DOMAIN/sign-in](http://YOUR_SITE_DOMAIN/sign-in)
3. Fill APInf settings [http://YOUR\_SITE\_DOMAIN/settings](http://YOUR_SITE_DOMAIN/settings)

## Mail {#mail}

The mail settings contain standard SMTP fields:

* **username** 
* **password**
* **host**
* **port**
* **from address** - used when sending emails
* **to address** - used for receiving emails, such as from the contact form

![](/assets/Apinf-settings-mail.png)

## Github {#github}

The Github configuration takes two values, a **Client ID** and **Secret key**. You can obtain these values by [setting up a Github application](https://developer.github.com/guides/basics-of-authentication/) from your Github user account.

![](/assets/Apinf-settings-github.png)

## Adding APIs {#adding-apis}

The **Adding APIs** section of the settings allows you to restrict the platform, so that only Admin users can add APIs.

![](/assets/Apinf-settings-addingAPIs.png)

## API Documentation Editor {#api-documentation-editor}

Apinf is able to integrate with the Swagger Editor. To enable the API Documentation Editor feature, you should have already deployed the Swagger Editor, so that it is accessible via an URL. Alternatively, you can link to the [Swagger Editor demo](http://editor.swagger.io/), assuming that it is accessible via HTTPS.

![](/assets/Apinf-settings-apiDocumentationEditor.png)

## SDK Code Generator {#sdk-code-generator}

Apinf integrates with the [Swagger Codegen](http://swagger.io/swagger-codegen/) project, allowing API Owners and Developers to generate SDK code based on a provided OpenAPI Specification file. To enable the SDK Code Generator feature, you should have already deployed the Swagger Codegen, so that it is accessible via an URL. Simply enter the Swagger Codegen URL in the **Host** field under **SDK Code Generator** settings panel and save settings.

![](/assets/Apinf-settings-sdkGenerator.png)

