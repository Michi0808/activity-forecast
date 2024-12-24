# Activity Forecast

This repository documents the integration workflows and automation tasks using n8n and Retool.

## Overview:

- Automates weather-based activity recommendations.
- Uses n8n for workflow automation and Retool for UI.

## Key Features:

1. **n8n Setup**:

   - Schedule Trigger at 8:00 AM daily.
   - Integration with Retool Webhook.

2. **Retool Integration**:
   - Activity recommendation based on OpenWeatherMap and OpenAI APIs.

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

## Detailed Logs:

For daily progress and detailed steps, refer to the [Logs directory](./logs/).

## Screenshots:

Screenshots are available in the [Screenshots directory](./screenshots/).
