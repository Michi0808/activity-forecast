# Activity Forecast

This repository documents the integration workflows and automation tasks using n8n and Retool.

## Overview:

- Provides weather-based activity recommendations through a Retool App, integrating weather data with actionable suggestions.
- Automates the process of generating and sending recommendations by linking n8n, Retool Workflow, and Airtable.
- Supports scheduled execution, dynamically fetching data from Airtable to enhance automation and flexibility.

## Key Features:

1. **Retool App for Weather-Based Recommendations**:

   - Leverages OpenWeatherMap API to fetch real-time weather data and Retool AI to generate activity suggestions based on ideal conditions.
     ![Retool App Interface](/screenshots/retool-app.png)

2. **n8n Workflow Automation**:

   - Configured Schedule Trigger to execute workflows daily at 8:00 AM automatically.
   - Integrates with Retool Workflow for seamless data processing and communication.
   - Fetches and processes records dynamically from Airtable to support flexible, real-time updates.
     ![n8n Workflow Setup](/screenshots/n8n-airtable-get-node.png)

3. **Retool Workflow Integration**:

   - Connects with OpenWeatherMap API to retrieve detailed weather data (e.g., temperature, humidity, wind speed).
   - Utilizes OpenAI for generating ideal weather conditions and activity recommendations.
   - Sends customized email reports, including weather insights and tailored activity suggestions.
     ![Retool Workflow Setup](../screenshots/retool-workflow.png)
     ![Email Example](/screenshots/full-email-success.png)

4. **Airtable Integration for Dynamic Inputs**:
   - Airtable serves as a dynamic data source for city, activity, and email address inputs.
     ![Airtable Table Setup](/screenshots/airtable-table-setup.png)

## Update History:

- **2024-12-20**:

  - Installed n8n via Node.js.
  - Created a Schedule Trigger to run daily at 8:00 AM (JST).
  - Tested the Schedule Trigger successfully.

- **2024-12-21**:

  - Configured a Set Node in n8n to define `city` ("Tokyo") and `activity` ("Hiking").
  - Successfully tested the Set Node to verify data output.
  - Attempted to create a Webhook resource in Retool, but it was unavailable.
  - Created a `REST API` resource in Retool as an alternative to the Webhook.

- **2024-12-22 to 24**:

  - Successfully integrated n8n with Retool Workflow to display and process data (`city` and `activity`).
  - Retrieved weather information from OpenWeatherAPI and sent it via email using Retool.
  - Added functionality to generate ideal weather conditions and activity recommendations with Retool AI.
  - Enhanced email content to include activity suggestions and sent a complete report.
  - Attempted to connect n8n with Google Sheets for dynamic input values but encountered authentication issues.

- **2025-01-10 to 11**:

  - Switched to Airtable as a data source after authentication issues with Google Sheets.
  - Created an Airtable table to store `City`, `Activity`, and `Email Address` data.
  - Successfully tested Airtable API with POSTMAN to fetch records and integrated it into n8n.
  - Updated n8n workflow to dynamically use Airtable data instead of static JSON.
  - Verified end-to-end workflow, ensuring Retool Workflow processed Airtable data and emails were sent correctly.

## Detailed Logs:

For daily progress and detailed steps, refer to the [Logs directory](./logs/).

## Screenshots:

Screenshots are available in the [Screenshots directory](./screenshots/).
