# Welcome
## This repository contains a basic LLM which I have traing on some lil wayne lyrics

### Special thanks to Andrej Karpathy
### and his video at: https://www.youtube.com/watch?v=kCc8FmEb1nY



## Results

Using Karpathy's initial training shakespear dataset I produced the following: 

### Initial training with shakespear dataset
#### Here is the parameters losses
 - 10.702913 M parameters
 - step 0: train loss 4.1498, val loss 4.1521
 - step 500: train loss 2.1906, val loss 2.2049
 - step 1000: train loss 2.0205, val loss 2.0848
 - step 1500: train loss 1.9077, val loss 2.0109
 - step 2000: train loss 1.8310, val loss 1.9509
 - step 2500: train loss 1.7718, val loss 1.9182
 - step 3000: train loss 1.7225, val loss 1.8872
 - step 3500: train loss 1.6758, val loss 1.8286
 - step 4000: train loss 1.6619, val loss 1.8261
 - step 4500: train loss 1.6265, val loss 1.7787
 - step 4999: train loss 1.6132, val loss 1.7725


#### Here is the ouput of 500 characters
```
GLOUCESTER:
Yet got there speak; glittless, I donne's fatter
Of our peoffort; a lathlike grust time.
Dawerst your me, as decraid her day your wind she fet vence pleason senders.

WAGREMNENIA:
My lord: growes yould, No,
Excurdease, a let yet so take he fears;
And help's figer, being in plearies'.

GLOUCESTER:
Fortwe though and my all plucier
Sity becone cannot, which nor let she but donoth thee rangerous othand that
What the revenisons and my bedin, not so goods,
Andim fiveing the gentle eaven wa
```


After training with a dataset of lil wayne lyrics this is what I was able to produce:
### Initial training with Lil Wayne Dataset

#### Here are the parameters and losses:

- 10.712141 M parameters
- step 0: train loss 4.5333, val loss 4.5342
- step 500: train loss 1.9465, val loss 2.1218
- step 1000: train loss 1.7172, val loss 2.0260
- step 1500: train loss 1.5511, val loss 1.9526
- step 2000: train loss 1.4030, val loss 1.9767
- step 2500: train loss 1.2649, val loss 1.9471
- step 3000: train loss 1.1550, val loss 1.9772
- step 3500: train loss 1.0566, val loss 2.0005
- step 4000: train loss 0.9579, val loss 2.0307
- step 4500: train loss 0.8836, val loss 2.0557
- step 4999: train loss 0.8089, val loss 2.1306
#### Here is the output from 500 characters:
```
Your lubressedle spitt drink 22" writing
Now, go Dirtore the han ble fuck and Cita—Coup an(T have I havi!
Phat eest, I with I'm bear
Plaze I go fuck 'Wayne is build, bitch
Some say sweet him, chrome and the night She neez the can suite me, bitch
And I'mma blazing ling Goding, but I aing baby di times ocen the car angel?
When  gave everybody it will don't reder so be check
Shood go gonna be? So h, drop it like it like itch
Savide it's hitch the being sunring carked up
Young Srite kur you wanna fu

```


I produced these results with:

batch_size = 16 # how many independent sequences will we process in parallel?
block_size = 32 # what is the maximum context length for predictions?
max_iters = 5000
eval_interval = 500
learning_rate = 3e-4
device = 'cuda' if torch.cuda.is_available() else 'cpu'
eval_iters = 200
n_embd = 384
n_head = 6
n_layer = 6
dropout = 0.2

as Hyper Parameters which took my 7 year old rtx-2070 about 30 minutes to train with a training set character count of
~65,000. 
