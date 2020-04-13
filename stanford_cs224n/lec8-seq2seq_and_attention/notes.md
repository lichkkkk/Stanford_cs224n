## Neural Machine Translation
### Seq2Seq problems
like machine translation, conversation, summarization.

### Seq2Seq Architecture
Encoder => fixed size context vector => Decoder.
Encoder uses usually LSTM, and Decider uses LSTM ,too.

### Training
TODO

## Attention
### Motivation
The single context vector may be a bottleneck: cannot hold all the information
and cannot help the decoder focus on the specific part of input.

### Architecture
Use attention score and attention output to help decider.
TODO: more details.
