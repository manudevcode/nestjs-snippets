<div style="text-align: center">
  <h1>Nest JS Snippets</h1>
  <img src="https://raw.githubusercontent.com/manudevcode/nestjs-snippets/main/images/icon.png" alt="Bits Theme for JavaScript" />
  
  Simple snippets pack to increase your productivity when developing with nestjs   
</div>
<br/>
<p align="center">
  <img alt="Marketplace" src="https://vsmarketplacebadge.apphb.com/version-short/ManuCodes.nestjs.snippets.svg?style=for-the-badge&color=df85ff&labelColor=384357"/>
  <img alt="Installs" src="https://vsmarketplacebadge.apphb.com/installs-short/ManuCodes.nestjs.snippets.svg?style=for-the-badge&color=df85ff&labelColor=384357">
  <img alt="Rating" src="https://vsmarketplacebadge.apphb.com/rating-short/ManuCodes.nestjs.snippets.svg?style=for-the-badge&color=df85ff&labelColor=384357">
</p>
<br/>

Created by [Manu Codes](https://github.com/manudevcode)

---

## Installation

The snippets is available in the VS Code marketplace. Search **NestJS Snippets**, install and go!

## Usage
<br/>

|  Prefix | Method                                              |
| ------: | --------------------------------------------------- |
|  `nestcon→` | Create new simple nest controller  |
|  `nestcrud→` | Create new CRUD controller |
|  `nestdel→` | Create a Delete method |
|  `nestget→` | Create a Get method |
|  `nestgetparam→` | Create a Get method with url param |
|  `nestpost→` | Create a Post method |
|  `nestput→` | Create a Put method |
|  `nestmid→` | Create a middleware class |
|  `nestguard→` | Create a guard class |
|  `nestschema→` | Create new mongodb schema |
|  `nestcron→` | Create new shcedule class to use crons |

## Examples
<br/>

This is the result of typing `nestcon` and press enter on your nest .ts file:

```ts
import { Controller } from '@nestjs/common';

@Controller('utl')
export class MyController {
	constructor() {}
}
```

This is the result of typing `nestgetparam` and press enter on your nest .ts file:

```ts
@Get('/:param')
async name(@Param('param') param: any, @Req() req: any, @Res() res: Response){
	// Put your magic here
}
```

This is the result of typing `nestschema` and press enter on your nest .ts file:

```ts
import { Prop, Schema, SchemaFactoryx} from '@nestjs/mongoose';
import { Document } from 'mongoose';

export type MySchemaDocument = MySchema & Document;
@Schema({
	 // timestamp: true
})
export class MySchema {
	@Prop()
	propName: string;

	// More props here
}

export const MySchemaSchema = SchemaFactory.createForClass(MySchema);

```