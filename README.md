<div style="display:flex; align-items: center;">

# 한국화학공학회 2022년도 봄 총회 및 학술대회_화학공학의 뉴노멀을 선도하다: 지속가능성과 에너지_기계학습 학생 구두 발표_ https://www.kiche.or.kr/files/202204121.pdf 
# Optimal Planning of Hybrid Energy Storage Systems using Curtailed Renewable Energy through Deep Reinforcement Learning_https://arxiv.org/pdf/2212.05662.pdf
# 한국화학공학회 2022년 봄 학술대회_화학공학소재연구정보센터_동영상 135개 조회수 1,495회 최종 업데이트: 2022. 10.
# https://youtube.com/playlist?list=PLAoNaLeYSkPu_hvSRSQUfNckz6AMrZ53b&si=UvCzeVOyBqOeQGWw
# Optimal Planning of Hybrid Energy Storage Systems using Curtailed Renewable Energy through Deep Reinforcement Learning

</div>

EMSRL is a reinforcement learning PPO algorithm designed to maximize profits by utilizing battery energy storage systems (BESS) and alkaline water electrolyzers (AWE) to manage curtailed energy generated from solar and wind power.

This model is described in the paper: [Optimal Planning of Hybrid Energy Storage Systems using Curtailed Renewable Energy through Deep Reinforcement Learning](https://arxiv.org/abs/2212.05662)




## setup

```
setup(
    name="EMSRL",
    version="1.0",
    url="https://github.com/kangdj6358/EMSRL",
    author="Dongju Kang, Doeun Kang",
    license="MIT",
    install_requires=[
        "gym == 0.18.3",
        "ray == 1.9.0",
        "ray[rllib] == 1.9.0",
        "pandas == 1.3.3",
        "openpyxl == 3.0.9",
        "torch == 1.9.1",
    ],
    zip_safe=False,
)
```

## Code implementation example

### Train EMSRL

You can adjust the hyperparameters in the rl_config in the train_EP.py file.

To train the dataset using PPO, please run

```
python EMSRL_train_EP.py
```

### Evaluate the result from checkpoint

After train the data, you can evaluate the results by:

```
python evaluate_EP.py results/{episode}/PPO/PPO_EMSRLEnv_{}/checkpoint_{000000}/checkpoint-{00} --run PPO --env EMSRLEnv --episodes {0000}
```

## Data

Datasets related to this article can be found at [California ISO](http://www.caiso.com/informed/Pages/ManagingOversupply.aspx)
