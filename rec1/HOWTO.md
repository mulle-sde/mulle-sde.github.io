# Record commands

`script -ttimings`

# Edit commands

```
teseq -ttimings typescript > session.tsq
subl session.tsq
```

# Replay commands

`reseq session.tsq --replay`

# Record with asciinema

```
asciinema rec -i 1 demo.cast
$ reseq session.tsq --replay
$ exit
```

