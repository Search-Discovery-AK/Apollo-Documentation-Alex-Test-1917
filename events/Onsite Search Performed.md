# Onsite Search Performed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Onsite Search Performed",
    "onsiteSearch": {
        "capacity": {
            "people": {
                "numAdults": "<numAdults>",
                "numChildren": "<numChildren>"
            }
        },
        "keyword": {
            "searchTerm": "<searchTerm>",
            "searchType": "<searchType>"
        },
        "location": {
            "map": {
                "zoomLevel": "<zoomLevel>"
            }
        },
        "scheduling": {
            "endDate": "<endDate>",
            "requestedDatesCount": "<requestedDatesCount>",
            "startDate": "<startDate>"
        }
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|endDate|string|End date requested. ISO 8601 form \(YYYY-MM-DD\). Jan 1, 2019 is 2019-01-01|2001-12-22, 2011-01-01|^([0-9]{4})-(1[0-2]|0[1-9])-(3[01]|0[1-9]|[12][0-9])$||||||
|numAdults|integer|Integer number of adults for the booking|1, 2, 3, 4, 5||||1|||
|numChildren|integer|Integer number of kids for the booking|1, 2, 3, 4, 5||||0|||
|requestedDatesCount|integer|Integer Number of days requested.|8, 1, 5, 6, 7, 10||||1|||
|searchTerm|string|Describes the search keyword used after auto-correct, auto-complete, or keyword suggestion. |bluth, blue, red lobster|||||||
|searchType|string|Describes the domain of the search. |products, properties, articles, authors, coupons, publications|||||||
|startDate|string|Start date requested. ISO 8601 form \(YYYY-MM-DD\). Jan 1, 2019 is 2019-01-01|2001-12-22, 2011-01-01|^([0-9]{4})-(1[0-2]|0[1-9])-(3[01]|0[1-9]|[12][0-9])$||||||
|zoomLevel|string|Indicator of the zoom level in a map presentation. Values are typically integers, but can vary depending on the map service used. |1, 2, 3, 4, 5, 6|||||||



