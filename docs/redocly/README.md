## Guide to host Swagger API documentation with GitHub Pages using redocly

[View most recent version on Tango.us](https://app.tango.us/app/workflow/f919b805-2603-4365-8343-ba3afac2d78a?utm_source=magicCopy&utm_medium=magicCopy&utm_campaign=workflow%20export%20links) or at **tutorial.html**
Please read the tutorial before moving to more advanced alternations 

In repo, there is also an additional file named "fancy\_dist.json" to add more features for your github page (error messages, request/response samples, distinct parameters etc)

### Merge API descriptions

To merge multiple API descriptions, you need to use the [redocly-cli](https://redocly.com/docs/cli/) 

To install Redocly, you'll need to use npm (Node Package Manager) since Redocly is a set of tools for working with APIs and documentation, and it's built on top of Node.js. Here are the general steps to install Redocly using npm:

1. **Node.js and npm:**
   Make sure you have Node.js and npm installed on your machine. You can download and install them from the official website: [Node.js Downloads](https://nodejs.org/).

2. **Create a new Node.js project (if needed):**
   If you don't have an existing Node.js project, you can create a new one by running the following commands in your terminal or command prompt:

   ```bash
   mkdir my-redocly-project
   cd my-redocly-project
   npm init -y
   ```

   This will create a new `package.json` file in your project folder.

3. **Install Redocly CLI:**
   Run the following command to install Redocly CLI globally on your machine:

   ```bash
   npm install -g @redocly/openapi-cli
   ```

   This installs the Redocly OpenAPI CLI tool globally, allowing you to use it from any directory in your terminal.

4. **Verify Installation:**
   You can verify the installation by running:

   ```bash
   redocly --version
   ```

   This should print the installed Redocly CLI version.

Keep in mind that the installation steps may vary slightly depending on your operating system and specific setup. It's always a good idea to check the official documentation for any updates or changes: [Redocly CLI Documentation](https://redoc.ly/docs/cli/).

After that, you use the **join** command to merge different API descriptions (e.g api1.yaml , api2.yaml) into a single one (e.g epi_join.yaml):

```bash
redocly join api1.yaml api2.yaml -o api-join.yaml
```

Το see a preview of your API specification in your browser (e.g at port 3000):
```bash
redocly preview-docs api-join.yaml --port 3000
```
