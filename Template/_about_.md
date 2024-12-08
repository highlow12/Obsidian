<%*
// 현재 노트의 폴더 경로 가져오기
const currentFile = tp.file.folder(true);

// 같은 폴더에 있는 모든 파일 목록 가져오기
const folderFiles = app.vault.getFiles().filter(file => 
    file.path.startsWith(currentFile) && 
    file.path !== tp.file.path(true)
);

// 파일들을 알파벳순으로 정렬
folderFiles.sort((a, b) => a.basename.localeCompare(b.basename));

// 링크 생성
let linkList = folderFiles.map(file => `- [[${file.basename}]]`).join('\n');

// 결과 출력
tR += `## 같은 폴더의 파일들\n\n${linkList}`;
%>