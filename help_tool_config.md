## Overview

This guide provides an overview of how to configure the **Message Context Protocol Tool** for various use cases. The tool supports different types of handlers that allow integration with native code, scripts, or file system operations. Understanding the configuration options is crucial for setting up your workflow effectively.

---

#### **1. Tool Types**

The Message Context Protocol Tool supports several types of tool configurations. Each type is designed for specific use cases:

- **File Resource Handler [internal]**  
  This type is used for managing file system operations such as listing files in a directory, reading files, or writing files. It is ideal for tasks that involve direct interaction with the file system.

- **Custom Tool Handler**  
  This type is intended for native applications written in languages like C++ or Objective-C. It allows you to integrate custom plug-ins into your workflow. The SDK provided by the App facilitates the installation of these plug-ins.

- **Script Tool Handler**  
  This type enables the execution of JavaScripts. The App provides a built-in editor for writing and managing scripts. This is useful when you need to perform dynamic operations using scripting.

---

#### **2. Method Name**

The method name specifies the action to be performed by the tool. The available methods depend on the selected tool type:

- **List files in a directory**  
  Available if the tool type is **File Resource Handler**. This method lists all files within a specified directory.

- **Read file from file system**  
  Available if the tool type is **File Resource Handler**. This method reads the content of a file from the file system.

- **Write file to file system**  
  Available if the tool type is **File Resource Handler**. This method writes data to a file on the file system.

- **Custom Tool**  
  Available if the tool type is **Custom Tool Handler** or **Script Tool Handler** with a predefined script entry point named `toolEntry`. This method executes a custom function defined in your plugin or script.

---

#### **3. Handler Name**

The **Handler Name** is a string identifier that helps track and manage the workflow process. It should be descriptive enough to identify the purpose of the handler in your application's context.

---

#### **4. Input Schema and Output Schema**

The **Input Schema** defines the structure of the data that the tool expects as input. The **Output Schema** defines the structure of the data that the tool will return.

### Example:
- **Type:** `object`
- **Properties:**
  - `files`: `array`  
    Contains a list of found source code files. Each file object includes:
    - `project_path`: `string`  
      The project directory used.
    - `last_modified`: `string`  
      The last modified date (ISO 8601 format).
    - `total_files`: `number`  
      Total number of files found.
    - `path`: `string`  
      Absolute path to the file.
    - `relative_path`: `string`  
      Relative path from the project directory.
    - `size`: `number`  
      File size in bytes.
  - `data`: `string`  
    Additional data returned by the tool.
  - `error`: `string`  
    Any error messages generated during execution.

---

#### **5. Configuration Steps**

1. **Select the Tool Type**  
   Choose the appropriate tool type based on your needs:
   - Use **File Resource Handler** for file system operations.
   - Use **Custom Tool Handler** for native code integration.
   - Use **Script Tool Handler** for JavaScript execution.

2. **Set the Method Name**  
   Based on the selected tool type, choose the corresponding method:
   - For **File Resource Handler**, select one of the file system operations.
   - For **Custom Tool Handler** or **Script Tool Handler**, use **Custom Tool**.

3. **Define the Handler Name**  
   Enter a descriptive string to identify the handler in your workflow.

4. **Configure Input and Output Schemas**  
   Ensure that the input schema matches the expected data format. The output schema should define the structure of the data returned by the tool.

5. **Save and Test**  
   After configuring the tool, save the settings and test the workflow to ensure it functions as expected.

---

By following this guide, you can effectively configure the Message Context Protocol Tool to meet your specific requirements. Whether you are working with file system operations, custom native code, or JavaScript scripts, the tool provides a flexible and powerful solution.
