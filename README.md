Repository for my github page. To see the page, click [here](https://thomick.github.io/).

## Reminder for myself

To run the page locally, use the following command:

```bash
docker build -t jekyll-site .
docker run -p 4000:4000 --rm -v $(pwd):/usr/src/app jekyll-site
```
