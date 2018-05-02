## tensorflow.js

* Python was considered the best programming language for machine learning and AI stuff.
* Though we can still do it in other programming language Python was considered best for it's ease and devloper community.
* javaScript is considered most popular language for over two decades as it rules the web.

- Google's tensorflow was one of the best resourse held by Python.
- Recently tensorflow team released a javaScript version.

## install

* we can get it from the tensorflow.js team.

#### CDN

`<!-- Load TensorFlow.js -->
<script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@0.10.0"> </script>`

#### use

HTML code
`
<html>
  <head>
    <!-- Load TensorFlow.js -->
    <script src="https://cdn.jsdelivr.net/npm/@tensorflow/tfjs@0.10.0"> </script>

    <!-- Place your code in the script tag below. You can also use an external .js file -->
    <script>
      // Notice there is no 'import' statement. 'tf' is available on the index-page
      // because of the script tag above.

      // Define a model for linear regression.
      const model = tf.sequential();
      model.add(tf.layers.dense({units: 1, inputShape: [1]}));

      // Prepare the model for training: Specify the loss and the optimizer.
      model.compile({loss: 'meanSquaredError', optimizer: 'sgd'});

      // Generate some synthetic data for training.
      const xs = tf.tensor2d([1, 2, 3, 4], [4, 1]);
      const ys = tf.tensor2d([1, 3, 5, 7], [4, 1]);

      // Train the model using the data.
      model.fit(xs, ys).then(() => {
        // Use the model to do inference on a data point the model hasn't seen before:
        // Open the browser devtools to see the output
        model.predict(tf.tensor2d([5], [1, 1])).print();
      });
    </script>

  </head>

  <body>
  </body>
</html>
`

### npm, yarn

`yarn add @tensorflow/tfjs`

`npm install @tensorflow/tfjs`

#### use

in main.js file
`{js}
import \* as tf from '@tensorflow/tfjs';

// Define a model for linear regression.
const model = tf.sequential();
model.add(tf.layers.dense({units: 1, inputShape: [1]}));

// Prepare the model for training: Specify the loss and the optimizer.
model.compile({loss: 'meanSquaredError', optimizer: 'sgd'});

// Generate some synthetic data for training.
const xs = tf.tensor2d([1, 2, 3, 4], [4, 1]);
const ys = tf.tensor2d([1, 3, 5, 7], [4, 1]);

// Train the model using the data.
model.fit(xs, ys).then(() => {
// Use the model to do inference on a data point the model hasn't seen before:
model.predict(tf.tensor2d([5], [1, 1])).print();
});`
### Documentation 
https://js.tensorflow.org
