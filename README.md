# axesso-java-client

Axesso Api
- API version: 1.0.0
  - Build date: 2018-12-21T15:33:25.535Z

Use this api to fetch information to Amazon products and more.


*Automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen)*


## Requirements

Building the API client library requires:
1. Java 1.7+
2. Maven/Gradle

## Installation

To install the API client library to your local Maven repository, simply execute:

```shell
mvn clean install
```

To deploy it to a remote Maven repository instead, configure the settings of the repository and execute:

```shell
mvn clean deploy
```

Refer to the [OSSRH Guide](http://central.sonatype.org/pages/ossrh-guide.html) for more information.

### Maven users

Add this dependency to your project's POM:

```xml
<dependency>
  <groupId>de.axesso</groupId>
  <artifactId>axesso-java-client</artifactId>
  <version>1.0.0</version>
  <scope>compile</scope>
</dependency>
```

### Gradle users

Add this dependency to your project's build file:

```groovy
compile "de.axesso:axesso-java-client:1.0.0"
```

### Others

At first generate the JAR by executing:

```shell
mvn clean package
```

Then manually install the following JARs:

* `target/axesso-java-client-1.0.0.jar`
* `target/lib/*.jar`

## Getting Started

Please follow the [installation](#installation) instruction and execute the following Java code:

```java

import io.swagger.client.*;
import io.swagger.client.auth.*;
import io.swagger.client.model.*;
import io.swagger.client.api.AmzApi;

import java.io.File;
import java.util.*;

public class AmzApiExample {

    public static void main(String[] args) {
        
        AApiClient client = new ApiClient();
	client.setApiKey("XXXXXX");			//contact support@axesso.de to get key
	AmzApi apiInstance = new AmzApi(client);
        try {
            ProductDetailsResponse product = apiInstance.requestProduct("https://www.amazon.com/dp/B07TN8B972", null);
            System.out.println(product);
        } catch (ApiException e) {
            System.err.println("Exception when calling AmzApi#requestProduct");
            e.printStackTrace();
        }
    }
}

```

## Documentation for API Endpoints

All URIs are relative to *http://api.axesso.de*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AmzApi* | [**keywordSearch**](docs/AmzApi.md#keywordSearch) | **GET** /amz/amazon-search-by-keyword | fetch results auf a keyword search on Amazon
*AmzApi* | [**requestBuyRecommendation**](docs/AmzApi.md#requestBuyRecommendation) | **GET** /amz/amazon-lookup-buy-recommendations | request buy recommendations to a given product
*AmzApi* | [**requestProduct**](docs/AmzApi.md#requestProduct) | **GET** /amz/amazon-lookup-product | lookup product information
*AmzApi* | [**sortOptions**](docs/AmzApi.md#sortOptions) | **GET** /amz/sort-options | request available sort options to use in keyword search


## Documentation for Models

 - [BuyRecommendationResponse](docs/BuyRecommendationResponse.md)
 - [KeywordSearchResponse](docs/KeywordSearchResponse.md)
 - [ProductDetailsResponse](docs/ProductDetailsResponse.md)
 - [SortOptionResponse](docs/SortOptionResponse.md)
 - [SortOptionResponseSortOptions](docs/SortOptionResponseSortOptions.md)


## Documentation for Authorization

All endpoints do not require authorization.
Authentication schemes defined for the API:

## Recommendation

It's recommended to create an instance of `ApiClient` per thread in a multithreaded environment to avoid any potential issues.

## Author

support@axesso.de

