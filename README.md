# dogact
dogact is UI libary cloning react for **study**.

## usage

```
import { createDOM, render, makeElement } from "./dogact.js";

const h1 = makeElement('h1');
const div = makeElement('div');
const ul = makeElement('ul');
const li = makeElement('li');

const List = () => {
    return (
        ul({},
            li({style: "color:red"}, "1st item"),
            li({style: "color:blue"}, "2nd item"),
            li({style: "color:green"}, "3rd item"),
        )
    )
}
const App = () => {
    return (
        div( {},
            h1( {}, "Dogact start"),
            List()
        )
    );
};


render('#root', createDOM(App()));
```