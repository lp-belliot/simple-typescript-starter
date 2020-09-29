# 🧰 Simple TypeScript Starter | 2020

> We talk about a lot of **advanced Node.js and TypeScript** concepts on [the blog](https://khalilstemmler.com), particularly focused around Domain-Driven Design and large-scale enterprise application patterns. However, I received a few emails from readers that were interested in seeing what a basic TypeScript starter project looks like. So I've put together just that.

### Scripts

#### `npm run start:dev`

Starts the application in development using `nodemon` and `ts-node` to do hot reloading.

#### `npm run build`

Builds the app at `build`, cleaning the folder first.

#### `npm run start`

Starts the app in production by first building the project with `npm run build`, and then executing the compiled JavaScript at `build/index.js`.


# Domain Structure
## Player - Aggregate Root
Contains logic about which entity you can play cards from.
### Hand - CardCollection Entity
If you're on the deck and end your turn on less than 3 cards you have to pick up from the deck.
### FaceDown - CardCollection Entity
Can't access facedown until faceup and hand are empty.
### FaceUp - CardCollection Entity
Can't access faceup until hand is empty or faceup card can be played with last hand card.
