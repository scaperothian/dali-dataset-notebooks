# Notebooks and other Utilited for the DALI dataset
Jupyter notebooks for downloading and manipulating the DALI Dataset.  see [source repo](https://github.com/gabolsgabs/DALI) for more examples.

# Download DALI audio data

```python download.py --metadata_path="<abs path to data> --audio_path=<abs path where audio should go>```

Metadata refers to data pulled from Zenodo for the DALI dataset. There is a v1 and and v2 that are possible. when downloaded from Zenodo they have different names.  v1 has around 5358 songs and v2 has 7756.  

Audio is pulled from youtube that marries up with the metadata described above.  If there is a file that is represented by a uuid.log, this means the audio did not successfully download.  Audio is downloaded as a .wav file, however, no other constraints are put on the download, so more preprocessing should be done to normalize sample rates for example.

# Recommendations

Recommend that the metadata be saved directly in this repo as metadata_v1 or metadata_v2 depending on whether this is for DALI v1 or DALI v2.  

Likewise, saving the audio in the audio_path to the local directory as audio_v1 or audio_v2 depending on whether this is for DALI v1 or DALI v2.

The repo will ignore those conventions for git purposes (see .gitignore)