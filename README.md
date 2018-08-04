# Model-Based-Reinforcement-Learning
This is a project trying to build a model based reinforcement learning program using tensorflow to play atari games. The project will contain three parts: State Predictor, Action Predictor and the main program.

## State Predictor
State Predictor is the key part of model based reinforcement learning model by using which to simulate states to help the reinforcement learning model choose the best next action.Three different state predictors are inplemented based on http://people.ee.duke.edu/~lcarin/Kevin4.21.2017.pdf and http://cs231n.stanford.edu/reports/2016/pdfs/215_Report.pdf.

### Variational Autoencoders State Predictor
Compared with Action-Conditional video prediction models, VAE state predictor is designed to solve model stochasticity in some Artari games.

#### Model Structure
* `Encoder`: Three convolutional layers of kernal size 3, stride 2 and 128 outputs were used to to compress the input image.
* `Dimension of latent vector`: *Default*: `20`
* `Decoder`: Three deconvolutional layers of kernal size 3, stride 2 and 128 inputs channels.

<table align='center'>
<tr align='center'>
<td> Input image </td>
<td> VAE Prediction </td>
</tr>
<tr>
<td><img src = 'https://user-images.githubusercontent.com/31879289/43647852-6efd8044-976b-11e8-8542-369de79bcd40.png' height = '300px'>
<td><img src = 'https://github.com/waynecai2/Model-Based-Reinforcement-Learning/blob/master/VAE%20Predictions.png' height = '300px'>
</tr>
</table>

### Feedforward Encoding State Predictor
Action-Conditional Video Prediction,

#### Model Structure
* `Encoder`: Three convolutional layers of kernal size 3, stride 2 and 128 outputs were used to to compress the input image.
* `Dimension of latent vector`: Multiplicative interaction between encoded features and action control variables.
* `Decoder`: Three deconvolutional layers of kernal size 3, stride 2 and 128 inputs channels.

<table align='center'>
<tr align='center'>
<td> Input image </td>
<td> VAE Prediction </td>
</tr>
<tr>
<td><img src = 'https://user-images.githubusercontent.com/31879289/43647852-6efd8044-976b-11e8-8542-369de79bcd40.png' height = '300px'>
<td><img src = 'https://github.com/waynecai2/Model-Based-Reinforcement-Learning/blob/master/VAE%20Predictions.png' height = '300px'>
</tr>
</table>
