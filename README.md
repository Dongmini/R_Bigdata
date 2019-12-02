# R

### 김동민

# 저는 평범한 학생입니다.

### 빅데이터학과

# 빅데이터학과에서는 데이터를 다룹니다.

### 좋아하는 것들
+ 친구
  - 승훈이형

+ 애착 물건
  - 컴퓨터

+ 음식
  - 국밥

### 사진

![](dasd.jpg)

### 자료분석
### 지도 관련 패키지 설치 및 불러오기
# + 공간 지도 분석을 위한 패키지
# - maps: 세계 지도 데이터베이스
# - mapproj: 지도 상에 위도와 경도를 표시
# - ggplot2: map_data()를 이용하여 지도정보를 R로 불러오기
# - ggiraphExtra : 단계 구분도 표시

install.packages("maps")
install.packages("mapproj")
install.packages("ggiraphExtra")

library(maps)
library(mapproj)
library(ggplot2)
library(ggiraphExtra)


korea_map <- map_data("world", region = "South Korea", su)
head(korea_map)
str(korea_map)


map('world', region = c('South Korea', 'North Korea'), col='skyblue', fill=TRUE)
title("Korea map in maps packages", col='blue', fill=T)

map('world', region=c('South Korea'), col='blue', add = TRUE, fill = TRUE)
map('world', region=c('North Korea'), col = 'red', add = TRUE, fill = TRUE)


###  kormap2패키지 : 2014년 한국 행정 지도 (시군구별) 데이터 
# [참고]  https://rstudio-pubs-static.s3.amazonaws.com/222145_fdcc8a5cb9584950ae7e8097304bf398.html
install.packages("devtools")
update.packages(checkBuilt=TRUE)
devtools::install_github("cardiomoon/kormaps2014")
library(kormaps2014)


# 한국의 행정지도를 그리기 위한 패키지 불러오기
library(kormaps2014)  # 한국행정지도 데이터
# kormap1 : 2014년 한국행정지도(시도별)
# kormap2 : 2014년 한국행정지도(시군구별)
# kormap3 : 2014년 한국행정지도(읍면동별)
library(ggplot2)      # 그래프 그리기
library(ggiraphExtra) # 단계구분도 작성

library(dplyr)
library(stringr)

kormap2
str(kormap2)

### 자료 분석2
강원도 도시대기측정결과를 지도에 표현해보자.

### 지도 관련 패키지 설치 및 불러오기
# + 공간 지도 분석을 위한 패키지
# - maps: 세계 지도 데이터베이스
# - mapproj: 지도 상에 위도와 경도를 표시
# - ggplot2: map_data()를 이용하여 지도정보를 R로 불러오기
# - ggiraphExtra : 단계 구분도 표시

ggplot(economics, aes(x=date, y=pce)) + geom_line(color='red')

