# sentiment
An example repository for mini CI/CD machine learning project using github actions.
Full description in [my blog](https://yonigottesman.github.io/cicd/mlops/github/2021/02/04/mini-cicd-github-actions.html).


CI/CD workflow  
1. Model is happily served [here](http://sentiment-env.eba-pcptvp7e.us-west-2.elasticbeanstalk.com/predict?tweet=i%20have%20really%20good%20luck%20:\)).
2. Train and improve model.
3. Upload new model to s3.
4. Create pr with new code that points to new model on s3.
5. github-action test code and model on pr and creates a nice summary.
6. After review, merge pr to main.
7. github-action deploy model to production.
8. goto step 1.

Checkout [this](https://github.com/yonigottesman/sentiment/pull/15) pr. Tests have passed and a comment has been made to compare main model and new model on testset.

model served using FastAPI on aws elasticbeanstalk and deployed using [eb-deploy.yml](https://github.com/yonigottesman/sentiment/blob/main/.github/workflows/eb-deploy.yml)



