# Chart disease progression with the Weather Company Data Disease Tracker API

Tracking a disease's progression is incredibly useful in a pandemic like COVID-19. The Weather Company created a Data Disease Tracker API that allows you to track the progression of a disease for a given location. It provides information regarding active diseases including confirmed cases, deaths, and recoveries over a period of up to 60 days in the past. 

In this tutorial, I show you how to access the Weather Company Data Disease Tracker API endpoint in Python from Watson Studio (or Jupyter Notebook).

## Getting started

### Prerequisite

- [Register for an IBM Cloud account](https://cloud.ibm.com/registration).

### Steps

1. [Obtain a Weather Company API Key](#obtain-a-weather-company-api-key)
1. [Obtain a HERE Location Services API Key](#obtain-a-here-location-services-api-key)
1. [Import the notebook into IBM Watson Studio](#import-the-notebook-into-ibm-watson-studio)
1. [Run the notebook](#run-the-notebook)

#### Obtain a Weather Company API Key

If you're participating in the [Call for Code](https://developer.ibm.com/callforcode/) Global Challenge, you have access to The Weather Company API for COVID-19 Disease Tracking. 

Go to the [Call for Code Weather website](https://callforcode.weather.com/) and [register](https://callforcode.weather.com/register). A time-limited API key will be sent to you via email. The documentation for the Weather Company APIs for Call for Code can be found [here](https://callforcode.weather.com/documentation/).

#### Obtain a HERE Location Services API Key

When using the application, you may pass it a geocode (for example, '35.843686,-78.78548'), a postal key (for example, 90210:US), or an address. If you pass an address, the application will try to use HERE Location Services for geocoding.

To access the HERE Geocoding API, an API Key is required. Follow the instructions outlined in the [HERE Developer Portal](https://developer.here.com/ref/IBM_starterkit_Covid?create=Freemium-Basic) to generate a free [API Key](https://developer.here.com/documentation/authentication/dev_guide/topics/api-key-credentials.html).

#### Import the notebook into IBM Watson Studio

1. [Sign into IBM Watson Studio Cloud](https://dataplatform.cloud.ibm.com/auth/iamid/login?context=analytics)
1. [Create a project](https://dataplatform.cloud.ibm.com/docs/content/wsj/getting-started/projects.html)
1. From your project, click **Add to Project**
1. Select **Notebook**
1. On the **New Notebook** page, select **From URL**
1. Enter a **Name** for the notebook
1. For the **Notebook URL**, enter the URL for the notebook (found in [this GitHub repo](https://github.com/Call-for-Code/twc-disease-tracker-api-python)):

    ```
    https://raw.githubusercontent.com/Call-for-Code/twc-disease-tracker-api-python/master/twc-disease-tracker-api.ipynb
    ```

1. Click **Create**

The notebook should be uploaded into your project and opened up.

#### Run the notebook

From within the notebook:

1. Update the cell under the **Set API keys** section and set the Weather Company Data API key (i.e., `TWC_APIKEY`)
1. Update the cell under the **Set API keys** section and set the HERE Location services API key (i.e., `HERE_APIKEY`)
1. Run through the notebook and execute each cell

In the **Run** section of the notebook, you can set the location you want to get data for. The location can be a geocode (i.e., `42.3584,-71.0598`), postal key (i.e., `02109:US`), or an address (e.g., `Boston, MA`) if HERE AP Key is set.

Examine the **Add function to query TWC API to get most recent report** section to see how exactly disease tracking API endpoint is used.

## Conclusion

Now that you ran through the notebook you should know how to connect other notebooks or a Python application to The Weather Company API for COVID-19 Disease Tracking, you are equipped to extend your knowledge and find new and creative ways to fight the disease.

## Resources

[The Weather Company - COVID-19](https://weather.com/coronavirus)  
[Call for Code - The Weather Company](https://callforcode.weather.com/)  
[Call for Code - COVID-19](https://developer.ibm.com/callforcode/getstarted/covid-19/)  
[HERE - Geocoding and Search](https://developer.here.com/documentation#search_and_geocoding_section)  
[IBM Watson Studio](https://www.ibm.com/cloud/watson-studio)

## License

This code is licensed under Apache 2.0. Full license text is available in [LICENSE](https://github.com/Call-for-Code/twc-disease-tracker-api-python/blob/master/LICENSE).
