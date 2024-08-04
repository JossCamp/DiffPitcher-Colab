<img src="img\cover.png">

# A simple adaptation of Diff Pitcher to run on Google Colab

# Diff-Pitcher (PyTorch)

Official Pytorch Implementation of [Diff-Pitcher: Diffusion-based Singing Voice Pitch Correction](https://engineering.jhu.edu/lcap/data/uploads/pdfs/waspaa2023_hai.pdf)

🤗huggingface link: https://huggingface.co/Higobeatz/Diff-Pitcher

--------------------

Thank you all for your interest in this research project. I am currently optimizing the model's performance and computation efficiency. I plan to release a user-friendly version, either a GUI or a VST, in the first half of this year, and will update the open-source license.

If you are familiar with PyTorch, you can follow [Code Examples](#examples) to use Diff-Pitcher.

--------------------

Diff-Pitcher

- [Demo Page](#demo)
- [Todo List](#todo)
- [Instructions](#Instructions)
- [References](#references)
- [Acknowledgement](#acknowledgement)

## Demo

🎵 Listen to [examples](https://jhu-lcap.github.io/Diff-Pitcher/)

## Todo
- [x] Update codes and demo
- [x] Support 🤗 [Diffusers](https://github.com/huggingface/diffusers)
- [x] Upload checkpoints
- [x] Pipeline tutorial
- [ ] Merge to [Your-Stable-Audio](https://github.com/haidog-yaqub/Your-Stable-Audio)
- [ ] Audio Plugin Support
## Instructions
- Run: Clone Repo and install dependencies
- Run: Download Models
- Feel free to try:

  - template-based automatic pitch correction: [template_based_apc.py](template_based_apc.py)
    ```bibtex    
    Use a third reference voice to tune the input voice.
    --i: input voice path
    --r: reference voice path
    --o: output voice path
    !python template_based_apc.py --i "/content/DiffPitcher/voice.wav" --r "/content/DiffPitcher/guide.wav" --o output_template.wav


  - score-based automatic pitch correction: [score_based_apc.py](score_based_apc.py)
    ```bibtex
    Use a MIDI file as a reference to tune voices.
    --i: input voice path
    --r: reference MIDI path
    --o: output voice path
    !python score_based_apc.py --i "/content/DiffPitcher/voice.wav" --r "/content/DiffPitcher/guide.mid" --o output_score.wav
    
## References

If you find the code useful for your research, please consider citing:

```bibtex
@inproceedings{hai2023diff,
  title={Diff-Pitcher: Diffusion-Based Singing Voice Pitch Correction},
  author={Hai, Jiarui and Elhilali, Mounya},
  booktitle={2023 IEEE Workshop on Applications of Signal Processing to Audio and Acoustics (WASPAA)},
  pages={1--5},
  year={2023},
  organization={IEEE}
}
```

This repo is inspired by:

```bibtex
@article{popov2021diffusion,
  title={Diffusion-based voice conversion with fast maximum likelihood sampling scheme},
  author={Popov, Vadim and Vovk, Ivan and Gogoryan, Vladimir and Sadekova, Tasnima and Kudinov, Mikhail and Wei, Jiansheng},
  journal={arXiv preprint arXiv:2109.13821},
  year={2021}
}
```
```bibtex
@inproceedings{liu2022diffsinger,
  title={Diffsinger: Singing voice synthesis via shallow diffusion mechanism},
  author={Liu, Jinglin and Li, Chengxi and Ren, Yi and Chen, Feiyang and Zhao, Zhou},
  booktitle={Proceedings of the AAAI conference on artificial intelligence},
  volume={36},
  number={10},
  pages={11020--11028},
  year={2022}
}
```

## Acknowledgement

[Welcome to LCAP! < LCAP (jhu.edu)](https://engineering.jhu.edu/lcap/)

We borrow code from following repos:

 - `Diffusion Schedulers` are based on 🤗 [Diffusers](https://github.com/huggingface/diffusers)
 - `2D UNet` is based on [DiffVC](https://github.com/huawei-noah/Speech-Backbones/tree/main/DiffVC)
