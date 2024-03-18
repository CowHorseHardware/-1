
capacity = [1; 3; 5];% 注射器的容量
Bili= [0.8/1; 2/3; 3/3; 4/5; 5/5];% 比例（实际药液容量/注射器容量）
count= 10:10:180;% 次数范围
com = [];% 初始化
single_injection_dosage = [];
for i = 1:length(capacity)% 循环结构
  for j = 1:length(Bili)
    for k = 1:length(count)
single_dosage = Bili(j) / count(k); % 计算单次注射剂量
% 所有的组合以及单次注射剂量
com= [com; capacity(i), Bili(j), count(k)];
single_injection_dosage = [single_injection_dosage; single_dosage];
      end
  end
end
disp('所有可能的组合和单次注射剂量：');
disp(com);
disp(single_injection_dosage);
