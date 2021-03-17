
Recreates TS build errors with plivo 4.14.2

To recreate run `npm install` then `tsc`

Errors reproduced below,

```
node_modules/plivo/dist/resources/accounts.d.ts:61:5 - error TS2416: Property 'update' in type 'Subaccount' is not assignable to the same property in base type 'PlivoResource'.
  Type '(name: string, enabled: boolean) => Promise<UpdateSubAccountDetails>' is not assignable to type '(params: object, id: string) => Promise<any>'.
    Types of parameters 'name' and 'params' are incompatible.
      Type 'object' is not assignable to type 'string'.

61     update(name: string, enabled: boolean): Promise<UpdateSubAccountDetails>;
       ~~~~~~

node_modules/plivo/dist/resources/accounts.d.ts:69:5 - error TS2416: Property 'delete' in type 'Subaccount' is not assignable to the same property in base type 'PlivoResource'.
  Type '(cascade: boolean) => Promise<unknown>' is not assignable to type '(params: object) => Promise<any>'.
    Types of parameters 'cascade' and 'params' are incompatible.
      Type 'object' is not assignable to type 'boolean'.

69     delete(cascade: boolean): Promise<unknown>;
       ~~~~~~

node_modules/plivo/dist/resources/accounts.d.ts:96:5 - error TS2416: Property 'create' in type 'SubaccountInterface' is not assignable to the same property in base type 'PlivoResourceInterface'.
  Type '(name: string, enabled: boolean) => Promise<CreateSubAccountResponse>' is not assignable to type '(params: object) => Promise<any>'.

96     create(name: string, enabled: boolean): Promise<CreateSubAccountResponse>;
       ~~~~~~

node_modules/plivo/dist/resources/applications.d.ts:109:5 - error TS2416: Property 'create' in type 'ApplicationInterface' is not assignable to the same property in base type 'PlivoResourceInterface'.
  Type '(appName: string, params?: {} | undefined) => Promise<CreateApplicationResponse>' is not assignable to type '(params: object) => Promise<any>'.
    Types of parameters 'appName' and 'params' are incompatible.
      Type 'object' is not assignable to type 'string'.

109     create(appName: string, params?: {}): Promise<CreateApplicationResponse>;
        ~~~~~~

node_modules/plivo/dist/resources/call.d.ts:294:2 - error TS2416: Property 'create' in type 'CallInterface' is not assignable to the same property in base type 'PlivoResourceInterface'.
  Type '(from: string, to: string, answerUrl: string, params?: {} | undefined) => Promise<CreateCallResponse>' is not assignable to type '(params: object) => Promise<any>'.

294  create(from: string, to: string, answerUrl: string, params ? : {}): Promise < CreateCallResponse > ;
     ~~~~~~

node_modules/plivo/dist/resources/callFeedback.d.ts:20:5 - error TS2416: Property 'create' in type 'CallFeedbackInterface' is not assignable to the same property in base type 'PlivoResourceInterface'.
  Type '(callUUID: string, rating: string, issues?: never[] | undefined, notes?: string | undefined) => Promise<CallFeedbackResponse>' is not assignable to type '(params: object) => Promise<any>'.

20     create(callUUID: string, rating: string, issues?: never[], notes?: string): Promise<CallFeedbackResponse>;
       ~~~~~~

node_modules/plivo/dist/resources/endpoints.d.ts:98:5 - error TS2416: Property 'create' in type 'EndpointInterface' is not assignable to the same property in base type 'PlivoResourceInterface'.
  Type '(username: string, password: string, alias: string, appId: string) => Promise<CreateEndpointResponse>' is not assignable to type '(params: object) => Promise<any>'.

98     create(username: string, password: string, alias: string, appId: string): Promise<CreateEndpointResponse>;
       ~~~~~~

node_modules/plivo/dist/resources/media.d.ts:45:19 - error TS2314: Generic type 'Array<T>' requires 1 type argument(s).

45     upload(files: Array): Promise<UploadMediaResponse>;
                     ~~~~~

node_modules/plivo/dist/resources/messages.d.ts:91:15 - error TS2314: Generic type 'Array<T>' requires 1 type argument(s).

91      media_urls: Array;
                    ~~~~~

node_modules/plivo/dist/resources/messages.d.ts:109:2 - error TS2416: Property 'create' in type 'MessageInterface' is not assignable to the same property in base type 'PlivoResourceInterface'.
  Type '(src: any, dst: any, text: string, optionalParams?: object | undefined, powerpackUUID?: string | undefined) => Promise<MessageResponse>' is not assignable to type '(params: object) => Promise<any>'.

109  create(src: any, dst: any, text: string, optionalParams?: object, powerpackUUID?: string ): Promise < MessageResponse >;
     ~~~~~~

node_modules/plivo/dist/resources/phloMultipartyCall.d.ts:24:5 - error TS2416: Property 'update' in type 'PhloMultiPartyCall' is not assignable to the same property in base type 'PlivoResource'.
  Type '(action: string, triggerSource: string, to: string, role: string) => Promise<UpdateMultipartyCallResponse>' is not assignable to type '(params: object, id: string) => Promise<any>'.

24     update(action: string, triggerSource: string, to: string, role: string): Promise<UpdateMultipartyCallResponse>;
       ~~~~~~

node_modules/plivo/dist/resources/phloMultiPartyCallMember.d.ts:27:5 - error TS2416: Property 'get' in type 'PhloMultiPartyCallMemberInterface' is not assignable to the same property in base type 'PlivoResourceInterface'.
  Type '(phloId: string, nodeId: string, memberAddress: string) => any' is not assignable to type '(id: string, params?: {} | undefined) => Promise<any>'.

27     get(phloId: string, nodeId: string, memberAddress: string): any;
       ~~~

node_modules/plivo/dist/resources/powerpacks.d.ts:195:5 - error TS2416: Property 'create' in type 'PowerpackInterface' is not assignable to the same property in base type 'PlivoResourceInterface'.
  Type '(name: string, params?: {} | undefined) => Promise<CreatePowerpackResponse>' is not assignable to type '(params: object) => Promise<any>'.
    Types of parameters 'name' and 'params' are incompatible.
      Type 'object' is not assignable to type 'string'.

195     create(name: string, params?: {}): Promise<CreatePowerpackResponse>;
        ~~~~~~


Found 13 errors.

```