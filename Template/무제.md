```dataviewjs
const tasks = dv.pages('"' + dv.current().file.path + '"').file.tasks;

const totalTasks = tasks.length;
const completedTasks = tasks.filter(task => task.completed).length;

const completionPercentage = totalTasks > 0 
  ? Math.round((completedTasks / totalTasks) * 100) 
  : 0;

dv.paragraph(`📋 총 태스크: ${totalTasks}개
✅ 완료된 태스크: ${completedTasks}개
🚀 완료율: ${completionPercentage}%`);
```