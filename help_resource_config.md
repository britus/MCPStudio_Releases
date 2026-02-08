# Configuring a Resource

This guide will walk you through setting up a resource to provide server system information. Let’s get started.

## Step 1: Name Your Resource

Begin by giving your resource a clear and descriptive name. In this example, we’ll name it **System Information**. This name will help you and others identify the purpose of the resource at a glance.

## Step 2: Provide a Description

Next, add a brief description to explain what your resource does. For this configuration, enter: **Provides Server System Information**. This helps ensure clarity and understanding when managing multiple resources.

## Step 3: Set the Resource Type

Define the type of content your resource will provide. In this case, select **content** as the resource type. This indicates that the resource will deliver content data.

## Step 4: Define the MIME Type

Specify the format of the data your resource will return. Set the **MIME Type** to **application/json**. This ensures that the data is returned in JSON format, which is ideal for structured information.

## Step 5: Configure the URI

Set the Uniform Resource Identifier (URI) for accessing your resource. Enter **system://info** as the URI. This unique identifier allows the resource to be accessed via a specific path.

## Step 6: Assign Audience and Priority

Finally, define the audience and priority for your resource. Set the **Ann. Audience** to **user**, indicating that this resource is intended for user access. Set the **Ann. Priority** to **0.9**, which indicates a high priority for this resource announcement.

## Summary

You’ve successfully configured a resource to provide server system information. Here’s a quick summary of your configuration:

- **Name**: System Information
- **Description**: Provides Server System Information
- **Type**: content
- **MIME Type**: application/json
- **URI**: system://info
- **Ann. Audience**: user
- **Ann. Priority**: 0.9

With these settings, your resource is ready to be used within the Message Context Protocol. You can now proceed to integrate it into your application or system as needed.

---

**Note**: This configuration ensures that your resource is clearly defined, accessible, and prioritized appropriately. Use this template to create additional resources as needed.
