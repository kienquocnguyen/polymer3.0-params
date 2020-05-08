# Polymer 3.0 Params Example

#### Thanks to "Polymer App Toolbox - Starter Kit" demo

In my project i clone this demo to use it as an appereance of this project.
https://github.com/Polymer/polymer-starter-kit

## Setup

### Install

After you clone "Polymer 3.0 Params Example" as an demo you need to install it with yarn

    yarn install

## Overview

After install you need to run command yarn start to start the project.

    yarn start


#### In Source Code

![polymer3 0-params-2](https://user-images.githubusercontent.com/33189395/75601129-cad49d00-5aea-11ea-8312-d666f2fce2c1.jpg)

#### In Browser

![polymer3 0-params-1](https://user-images.githubusercontent.com/33189395/75601126-c14b3500-5aea-11ea-8122-ba53ccbf3abb.jpg)

## How It's Work

#### 1. Pass a params in an on click function

In this project I created an on click button to switch to page "my-view2".

![polymer3 0-params-3](https://user-images.githubusercontent.com/33189395/75601201-88f82680-5aeb-11ea-9126-24019d21fe97.jpg)

#### 2. In the on click function I have pass a parameter name "params" with value is "2"

![polymer3 0-params-4](https://user-images.githubusercontent.com/33189395/75601231-daa0b100-5aeb-11ea-825d-dae86c664ba3.jpg)

#### 3. Then I use a method call "getQueryParameters" to call our url parameter.

    getQueryParameters (str) {
    return (str || document.location.search).replace(/(^\?)/,'').split("&").map(function(n){return n = n.split("="),this[n[0]] = n[1],this}.bind({}))[0];
    }

![polymer3 0-params-5](https://user-images.githubusercontent.com/33189395/75601281-3ec37500-5aec-11ea-9a65-88799de6c041.jpg)

#### 4. I used connectedCallback to call our "getQueryPrameters".

_connectedCallback: Called when the element is added to a document. Can be called multiple times during the lifetime of an element.

Then I create a variable name "queryParams" equal "this.getQueryPrameters"

![polymer3 0-params-6](https://user-images.githubusercontent.com/33189395/75601360-d6c15e80-5aec-11ea-828f-dd99723d3af9.jpg)

Then I set the value of element which id is "test" equal with "queryPrams.params" (our url "params" value)

![polymer3 0-params-7](https://user-images.githubusercontent.com/33189395/75601422-7d0d6400-5aed-11ea-9892-f6507b062a2f.jpg)


## Final Results

![polymer3 0-params-8](https://user-images.githubusercontent.com/33189395/75601438-bf36a580-5aed-11ea-93d5-460b7810070d.jpg)

![polymer3 0-params-9](https://user-images.githubusercontent.com/33189395/75601465-02911400-5aee-11ea-93dc-142a9ce68380.jpg)


### Hope you enjoy my work :D
