# EasyCarousel

Easy to use carousel component for Angular 4

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.3.2.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).
Before running the tests make sure you are serving the app via `ng serve`.

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
https://www.usefuldev.com/blog/post/publishing-a-library-from-an-angular-cli-project

# Usage [for Angular CLI]

## Install easy-carousel
- in your project root folder, run: npm install easy-carousel --save

## Import Module 

- insert the bottom line at the top of app.module.ts
  import { EasyCarouselModule } from 'easy-carousel/build/easy-carousel.module'

- inser EasyCarouselModule.forRoot() into app.module.ts,  
@NgModule({
  import: [
    ...,
    EasyCarouselModule.forRoot(),
    ...
  ]
  ...
})

## Template
<easy-carousel [carouselInfo]="demo1CarouselConfig" (onNotifyCarouselSelected)="onCarouselDemo1Selected($event)"></easy-carousel>

- the configuration 'demo1CarouselConfig' is defined like in below 'Sample Configuration' section
- implement the function onCarouselDemo1Selected in the component .ts
  
## Sample Configuration
demo1CarouselConfig = 
{
  "looping": true,
  "ratioHW": 0.65,
  
  "maxWidth": 1200,
  "itemsInOneScreen": 3,
  "itemsInOneScreenGroups": [
    {
      "screenWidth": 600,
      "itemsInOneScreen": 2
    },
    {
      "screenWidth": 900,
      "itemsInOneScreen": 3
    },
    {
      "screenWidth": 1200,
      "itemsInOneScreen": 4
    }
  ],
  
  "animationDuration": 1.5,
  "itemOutlineColor": "white",
  "autoPlay": {
    "enable": true,
    "delay": 2000,
    "duration": 2000
  },
  "trnsactionEffect": "ease-in",
  "items": [
    {"id": 1, "img": "./assets/img/carousel/1.jpg", "name": "NAME 1", "desc": "desc 1"},
    {
      "items": [
        {
          "id": 2,
          "img": "./assets/img/carousel/2-1.jpg",
          "name": "NAME 2-1",
          "desc": "desc 2-1",
          "sizeRatio": {
            "width": 0.5,
            "height": 1
          },
          "positionRatio": {
            "x": 0,
            "y": 0
          }
        },
        {
          "id": 3,
          "img": "./assets/img/carousel/4.jpg",
          "name": "NAME 2-2",
          "desc": "desc 2-2",
          "sizeRatio": {
            "width": 0.5,
            "height": 0.5
          },
          "positionRatio": {
            "x": 0.5,
            "y": 0
          }
        },
        {
          "id": 17,
          "img": "./assets/img/carousel/10.jpg",
          "name": "NAME 2-3",
          "desc": "desc 2-3",
          "sizeRatio": {
            "width": 0.5,
            "height": 0.5
          },
          "positionRatio": {
            "x": 0.5,
            "y": 0.5
          }
        }
      ]
    },
  ...
  ],
    "carouselItemInfo": {
      "nameColor": "white",
      "descColor": "lightgray",
      "minFontSize": 15,
      "maxFontSize": 40,
      "nameFontFamily": "",
      "descFontFamily": "",
      "itemOutlineWidth": 3
    },
    "carouselChildItemInfo": {
      "color": "white",
      "descColor": "lightgray",
      "minFontSize": 10,
      "maxFontSize": 30,
      "nameFontFamily": "",
      "descFontFamily": "",
      "itemOutlineWidth": 2
    },
    "selectedItemInfo": {
      "padding": 20,
      "backdropColorRGBA": "rgba(90, 150, 150, 0.7)",
      "backgroundColorRGBA": "rgba(190, 0, 0, 0.5)",
      "selectedItemOutlineColor": "white",
      "selectedItemOutlineWidth": 3,
      "nameColor": "yellow",
      "descColor": "white",
      "detailsColor": "white",
      "minFontSize": 10,
      "maxFontSize": 30,
      "nameFontFamily": "",
      "descFontFamily": "",
      "detailsFontFamily": "",
      "boxShadow": "6px 6px 5px 0px rgba(31,28,31,1)",
      "closeButtonColor": "white",
      "closeButtonTextShadow": "1px 2px 3px #000000"
    }
}

## Configuration Details
- looping: move to left/right endlessly,  
- ratioHW: the ratio of height vs width for each carousel item
- maxWidth: The maxmium width of the carouse
- itemsInOneScreen: the account of carousel items display in one screen
- itemsInOneScreenGroups: dynamic number of on screen carousel items for different window's width. If this property is defined, then maxWidth and itemsInOneScreen don't need to be defined
- animationDuration: the carousel animation duration
- carouselItemInfo: define color, font-size and font-family of each carousel item
- carouselChildItemInfo: define color, font-size and font-family of each child carousel item
- autoPlay: 
    enable: true  - enable auto play or not 
    delay: - delay before auto play
    duration: - duration of auto play animation
- trnsactionEffect: carousel animation effect
- items: - define all carousel items. if a carousel item contains children, each child must define their sizeRatio and positionRatio, they are relative to the width and height of the parent carousel item.
- carouselItemInfo - carousel item text colors, mini-fontSize, max-fontSize, fint families, outline color and width
- carouselChildItemInfo - carousel child item text colors, mini-fontSize, max-fontSize, fint families, outline color and width
- selectedItemInfo - if this is defined, when click on carousel item, there will be a details layer displaying on the top of carousel, in the items, you can define an entry of selectedImg, which will be displayed in the left of the details layer. If selectedImg is not defined, it will use the img instead. 

## Sample project
https://github.com/franksongca/easy-carousel-demo

## How to create angular project by [Angular CLI]
- please refer to: https://github.com/angular/angular-cli

