<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [kibana-plugin-server](./kibana-plugin-server.md) &gt; [CapabilitiesSetup](./kibana-plugin-server.capabilitiessetup.md) &gt; [registerProvider](./kibana-plugin-server.capabilitiessetup.registerprovider.md)

## CapabilitiesSetup.registerProvider() method

Register a [CapabilitiesProvider](./kibana-plugin-server.capabilitiesprovider.md) to be used to provide [Capabilities](./kibana-plugin-server.capabilities.md) when resolving them.

<b>Signature:</b>

```typescript
registerProvider(provider: CapabilitiesProvider): void;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  provider | <code>CapabilitiesProvider</code> |  |

<b>Returns:</b>

`void`

## Example

How to register a plugin's capabilities during setup

```ts
// my-plugin/server/plugin.ts
public setup(core: CoreSetup, deps: {}) {
   core.capabilities.registerProvider(() => {
     return {
       catalogue: {
         myPlugin: true,
       },
       myPlugin: {
         someFeature: true,
         featureDisabledByDefault: false,
       },
     }
   });
}

```

