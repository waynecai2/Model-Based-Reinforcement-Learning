# Model-Based-Reinforcement-Learning
This is a project trying to build a model based reinforcement learning program using tensorflow to play atari games. The project will contain three parts: State Predictor, Action Predictor and the main program.

# State Predictor
State Predictor is the key part of model based reinforcement learning model by using which to simulate states to help the reinforcement learning model choose the best next action.

Three different state predictors are inplemented based on http://people.ee.duke.edu/~lcarin/Kevin4.21.2017.pdf and http://cs231n.stanford.edu/reports/2016/pdfs/215_Report.pdf.

## Variational Autoencoders State Predictor
VAE state predictor is designed to solve model stochasticity. Breakout and Berzer were used to test the performance of prediction power of VAE predictor.

![Screenshot]("https://user-images.githubusercontent.com/31879289/43647852-6efd8044-976b-11e8-8542-369de79bcd40.png" "VAE Prediction")
