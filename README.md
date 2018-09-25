This has been forked directly from https://github.com/hunkim/word-rnn-tensorflow with the explicit intention of creating a 'Joe Posset Review AI'.

For full documentation and possible updates check out the source repo above.

# Training Data

The training data, in ```data/tinyshakespeare/input.txt```, consists of Joe's reviews from the Radio Free Midwich music blog. They were selected by searching "joe murray on", "posset on", and "rfm on" with false positive removed. These searches are unlikely to be perfect so some reviews may have been missed. The copy/pasted text was then edited to remove titles, headers, and band/purchase links. What's left is purely Joe's review text.

# Usage Rights

The text was sourced from https://radiofreemidwich.wordpress.com with permission for this specific use granted by Joe personally. No further rights to this text are granted or implied. Feel free to play around but don't be a c_nt.

The rest of the code falls under the MIT license as per the original authors.

# Requirements
- [Tensorflow 1.1.0rc0](http://www.tensorflow.org)

# Basic Usage
To train with default parameters on the tinyshakespeare corpus, run:
```bash
python train.py
```

I have been generating text with the following command:
```bash
python sample.py --prime "Starting text" -n 250 --pick 2 --width 4
```
This gives the opening words (in prime), with a length of 250 words and uses 'beam search' (check out the original project for more info/options).

# Sample output



### Word-RNN (with beam search)
```
# python sample.py --prime "Guns N' Roses - Appetite for Destruction" -n 100 --pick 2 --width 4

Guns N' Roses - Appetite for Destruction

vibe Miles perfected on Kind of Blue. On ‘What all the kind of mille plateaux-shudder to create a fitter, leaner guest-blogger. I was sprouting.” appear this is a meta-narrative of sound squeal. A purgatory of sunshine. The inflammation of that warms up the Hall & Oates that have originally functions and play it as a sound of the ‘Spin/Off’ is no one of the world’s longest pendulum tape east to west across the teeth. Track two is a audience burr and dry and isolated. If you just I can be the sort of mille plateaux-shudder to be a fitter, leaner guest-blogger. I was sprouting.” “That’s a fan that makes me all crying into my ears as the fan of the ion drive, the picture. The prolific artist at the kind of traffic – they baffle up for tea, jab this all I can.
```
