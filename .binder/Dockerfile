# Dockerfile for mybinder.org
#
# Test this Dockerfile:
#
#     docker build -t programming-with-categories .
#     docker run --rm -p 8888:8888 --name programming-with-categories --env JUPYTER_TOKEN=x programming-with-categories:latest
#

FROM crosscompass/ihaskell-notebook:835f7a6bc233

USER root

RUN mkdir /home/$NB_USER/programming_with_categories
COPY notebook/*.ipynb /home/$NB_USER/programming_with_categories/
COPY notebook/img /home/$NB_USER/programming_with_categories/img
RUN chown --recursive $NB_UID:users /home/$NB_USER/programming_with_categories

USER $NB_UID

ENV JUPYTER_ENABLE_LAB=yes
