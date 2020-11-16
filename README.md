# fork on

[bpmn-js Modeler + Properties Panel Example](https://github.com/bpmn-io/bpmn-js-examples/tree/master/properties-panel)

## About

a activiti process designer with bpmn-js(To use, please test the compatibility by yourself!!!)

### change from the base repo

/app/index.js

```js
// import propertiesPanelModule from 'bpmn-js-properties-panel';
// import propertiesProviderModule from 'bpmn-js-properties-panel/lib/provider/camunda';
// import camundaModdleDescriptor from 'camunda-bpmn-moddle/resources/camunda.json';

import propertiesPanelModule from 'bpmn-js-properties-panel-activiti';
import propertiesProviderModule from 'bpmn-js-properties-panel-activiti/lib/provider/activiti';
import activitiModdleDescriptor from 'activiti-bpmn-moddle/resources/activiti.json';


var bpmnModeler = new BpmnModeler({
  container: canvas,
  propertiesPanel: {
    parent: '#js-properties-panel'
  },
  additionalModules: [
    propertiesPanelModule,
    propertiesProviderModule
  ],
  moddleExtensions: {
    // camunda: camundaModdleDescriptor,
    activiti: activitiModdleDescriptor
  }
});
```

## Usage

[see](https://github.com/bpmn-io/bpmn-js-examples/blob/master/properties-panel/README.md)
