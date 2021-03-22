## content/sample-aa

### 기본컨셉
- 초기 컨셉은 content 폴더에 items 폴더에 잡혀진 내용 그대로 탐검색이 되도록 한다.(items 내에 md 파일이 contents type 역할을 한다. ) 
- 다수의 item을 통해 탐검색을 구현에 필요한 데이터를 확보해야 함으로 alcohol item으로 테스트를 한다. 
- rclone을 쓰지 않고, 해당 폴더를 복붙해도 된다. 

### rclone
- https://rclone.org/install/

### dropbox에 있는 알콜 샘플 아이템을 콘텐츠 폴더로 옮깁니다. 로컬 폴더에 있는 정리되지 않은 파일을 dropbox로 옮깁니다.
```
$ rclone sync dropbox:/items/aa {hugoprojectName}/content/items/aa
$ rclone sync {hugoprojectName}/content/items/aa dropbox:/items/aa 
```

### ccwps 샘플 콘텐츠 파일을 드롭박스에서 휴고프로젝트 콘텐츠 폴더로 옮깁니다. 

```
$ rclone sync dropbox:/items {hugoprojectName}/content/items
$ rclone sync {hugoprojectName}/content/items dropbox:/items 
```

### hugo content 폴더에서 목적을 가지고, 해당 폴더를 분류합니다. 기존에 분류가 되어 있다면, 폴더채로 옮겨올 수 있습니다. 
- 분류한 이후에 동기화로 dropbox의 목록이 그대로 유지됩니다. 