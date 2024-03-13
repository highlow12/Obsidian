# 필요한 기능
- [x] csv 로딩
- [x] csv 파일 이름 저장
- [x] ScriptData 리턴하는 메소드

# Docs
- *싱글톤: ScriptLoadManager.Instance로 호출*
- `NowLoadedFilename`: 읽기 전용, 지금 로딩된 csv 파일의 이름을 리턴한다
- `LoadScriptData(string csvName)`: `csvName`이름의 파일을 로딩한다. `csvName`파일은 Asset/Resources/CSV 안에 존재해야 한다
- `ScriptData GetScriptData(int id)`: 로딩된 파일에서 `id`위치의 `ScriptData`클래스를 리턴한다