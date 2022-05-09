# Trouble Shooting

5/9 go.mod version issue

- gorm version 1.23.11 -> 1.21.13<br/>
  go mod tidy -> go mod download<br/>
  종속성 받을때 이제는 go mod download 로 받는게 좋을 것 같지만<br/>
  tidy가 문제가 아닐 수 있으므로 더욱 더 정확한 방법을 찾는 것이 중요<br/>
