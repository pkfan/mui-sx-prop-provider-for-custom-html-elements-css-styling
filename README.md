# The sx prop of MUI system for all HTML elements for custom styling
MUI prefer (sx) prop for styling, but custom html elemnt can be created with (Box component="div") component in MUI which may be confuse in readibilty.

MUI System's sx prop lets you avoid writing unnecessary styled-component code, and instead define styles directly within the component itself. This is especially useful for one-off components with custom designs.

 * MUI does not provide (sx) styling props for custom html element
 * (e.g h1, div, span, a, header, footer etc)
 *
 * So this file contains most common html element with MUI SX props styling
 *
 * remeber all html element is in capatilize form after (sx) props decorator
 * e.g. a -> A, div -> Div, span -> Span, header -> Header

### Usage of (sxHtmlElements.js)
```js
import { Span, Div, Img, H1 } from './html';

<Span 
  sx={{ padding: '10px', background: 'black', color: 'white' }}
>
   Span with SX prop styles
</Span>

<Div 
   sx={{ padding: '5px', width: '200px', height: '200px', border: '1px solid red' }}
 >
  Div with SX prop styles
</Div>

<Img 
  sx={{ width: '400px', display: 'flex' }} 
  src="pkfan-profile.jpg" 
  alt="pkfan" 
/>

<H1 
   sx={{ fontWeight: '600', fontSize: '18px', color: 'blue' }}
 >
    h1, h2, h3, h4, h5, h6
 </H1>

```
### Usage of (useSXpropProvider) custom hook
```js
import useSXpropProvider from './useSXpropProvider';

const Div = useSXpropProvider('div');

<Div 
   sx={{ padding: '5px', width: '200px', height: '200px', border: '1px solid red' }}
>
  Div with SX prop styles
</Div>

```

### Benefits for these utilities
* avoid using of styled-components API
* avoid using of style.css or style.scss for each component in MUI for custom components

## Example

#### (Box) component from Material UI
decrease readibility of code.

```js
import { Box } from '@mui/material';

<Box
  component="div"
  sx={{
    width: '400px',
    height: '400px',
    background: 'grey',
    display: 'flex',
    flexWrap: 'wrap',
    padding: '10px',
    margin: '50px',
    gap: '10px',
    '& > span': {
      width: '100px',
      height: '100px',
      background: 'red',
      borderRadius: '10px',
    },
  }}
>
  <Box component="span">Item</Box>
  <Box component="span">Item</Box>
  <Box component="span">Item</Box>
  <Box component="span">Item</Box>
  <Box component="span">Item</Box>
  <Box component="span">Item</Box>
  <Box component="span">Item</Box>
  <Box component="span">Item</Box>
</Box>
```

#### Custom Html elements with (sx prop) wraper
increase readibility of code.

```js
import { Section, Span } from './sxHtmlElements';

<Section
  sx={{
    width: '400px',
    height: '400px',
    background: 'grey',
    display: 'flex',
    flexWrap: 'wrap',
    padding: '10px',
    margin: '50px',
    gap: '10px',
    '& > span': {
      width: '100px',
      height: '100px',
      background: 'red',
      borderRadius: '10px',
    },
  }}
>
  <Span>Item</Span>
  <Span>Item</Span>
  <Span>Item</Span>
  <Span>Item</Span>
  <Span>Item</Span>
  <Span>Item</Span>
  <Span>Item</Span>
  <Span>Item</Span>
</Section>
```



#### Don't forget to give star on this repository, so that other can find it easily and use.

###### keywords
* How to add custom CSS in Material UI
* material ui usestyles
* Material UI override style
* What can I use instead of makeStyles in material UI?
* override material-ui css react
* Styling Material UI components using CSS
