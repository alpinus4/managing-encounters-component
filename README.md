# Component for managing encounters
Connected with this: https://gitlab.com/librehealth/gci/issues/80 GCI task.
Designed by me.

Tested on Firefox 57.0.4 and Chrome 63.0.3239.132.

## How to install?
1. #### Clone it via Git:
```
git clone https://github.com/alpinus4/managing-encounters-component
```
2. #### Download zip file:




## How to use?

1. Basic usage:
```html
<link rel="import" href="encounters-management.html"> <!-- In head-->
<encounters-management id="encounters_management_component_id" rest-url="http://localhost:8080/lh-toolkit/ws/rest/v1"/> <!-- In body-->
```
2. Custom CSS properties:
```css
#encounters_management_component_id {

  /*MAIN*/
  --encounters-management-display: inline-block;
  --encounters-management-font-size: 20pt;
  --encounters-management-font-color: rgb(24, 24, 24);
  --encounters-management-background-color: inherit;
  --encounters-management-padding: 20px;

  /*HEADER*/
  --encounters-management-font-size-header: 36pt;
  --encounters-management-font-color-header: rgb(62, 62, 62);

  /*PATIENT NAME HEADER*/
  --encounters-management-font-size-header-patient-name: 25pt;
  --encounters-management-font-color-header-patient-name: rgb(62, 62, 62);

  /*SEARCH BAR*/
  --encounters-management-search-bar-background-color: rgb(255, 255, 255);
  --encounters-management-search-bar-text-color: inherit);

  /*BUTTONS*/
  --encounters-management-button-background-color: rgb(255, 255, 255);
  --encounters-management-button-text-color: inherit;

  /*NUMBER OF RECORDS TEXT*/
  --encounters-management-font-color-records-count: rgb(62, 62, 62);
  --encounters-management-font-size-records-count: 15pt);

  /*MODAL*/
  --encounters-management-font-size-modal: 16pt;
  --encounters-management-font-color-modal: inherit;
  --encounters-management-modal-background-color: #fefefe;
  --encounters-management-font-size-modal-buttons: 16pt;
  --encounters-management-font-color-modal-buttons: inherit;

      /*MODAL ICON CLOSE*/
  --encounters-management-close-modal-icon-color: #aaaaaa;
  --encounters-management-close-modal-icon-color-focus-hover: #000;


/*///////////////////////////////////////////*/
/*///////////////IN TABLE///////////////////*/
/*///////////////////////////////////////////*/

  /*TABLE MAIN*/
  --encounters-management-table-stripes-background-color: rgb(255, 243, 228);
  --encounters-management-table-no-stripes-background-color: rgb(255, 255, 255);

  /*ENCOUNTER TYPE*/
  --encounters-management-font-size-type: inherit;
  --encounters-management-font-color-type: inherit;

  /*ENCOUNTER LOCATION*/
  --encounters-management-font-size-location: inherit;
  --encounters-management-font-color-location: inherit;

  /*ENCOUNTER DATETIME*/
  --encounters-management-font-size-datetime: inherit;
  --encounters-management-font-color-datetime: inherit;

  /*LOADING SPINNER*/
  --encounters-management-loading-spinner-color: #141414;
}
```

3. Properties usage:
  * `rest-url` - `String` you have to set it to your url to lh-toolkit rest api endpoint
  * `encounters` - `Array` all encounters downloaded from lh-toolkit, contains `Objects`
  * `encounters-to-display` - `Array` encounters currently displayed, contains `Objects`
  * `encounters-to-display-total-quantity` - `Number` total (from all pages) number of encounters to display
  * `search-query` - `String` search query at the beginning
  * `not-found` - `Boolean` true value if not found
  * `loading` - `Boolean` true value if loading
  * `page-nmb` - `Number` currently displayed page index
  * `filters` - `Boolean` true if enabled any filters
  * `available-locations` - `Array` list of all available locations downloaded from lh-toolkit
  * `available-types` - `Array` list of all available encounter types downloaded from lh-toolkit
  * `available-forms` - `Array` list of all available encounter forms downloaded from lh-toolkit
  * `available-encounter-roles` - `Array` list of all available encounter roles downloaded from lh-toolkit
