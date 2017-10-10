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

#Usage

## Template
<easy-carousel [carouselInfo]="demo1CarouselInfo" (onNotifyCarouselSelected)="onCarouselDemo1Selected($event)"></easy-carousel>

## Module (Sample data)
demo1CarouselInfo = 
{
  "maxWidth": 1200,
  "ratioHW": 0.65,
  "itemsInOneScreen": 3,
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
  "carouselItemColor": {
    "name": "white",
    "desc": "white"
  }
}

## Configuration Details

- maxWidth: The maxmium width of the carouse
- ratioHW": the ratio of height vs width for each carousel item
- itemsInOneScreen: the account of carousel items display in one screen
- animationDuration": the carousel animation duration
- itemOutlineColor": outline color of each carousel item
- autoPlay: 
    enable: true  - enable auto play or not 
    delay: - delay before auto play
    duration: - duration of auto play animation
- trnsactionEffect: carousel animation effect
- items: - define all carousel items. if a carousel item contains children, each child must define their sizeRatio and positionRatio, they are relative to the width and height of the parent carousel item.
- carouselItemColor - carousel item text colors

## Sample project
https://github.com/franksongca/easy-carousel-demo
