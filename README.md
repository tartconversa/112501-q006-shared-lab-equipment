# 基层检验设备共享资料基线

CSV 使用 UTF-8 编码，首行为字段名。资料仅提供项目所需的合成事实，空值代表来源尚未提供。

- `equipment.csv`：基线资料，首行为 `equipment,clinic,method,valid_from,state`。
- `samples.csv`：基线资料，首行为 `batch,clinic,method,collected_at,due_at,repeat_of`。
- `technicians.csv`：基线资料，首行为 `technician,qualification,date,route,minutes`。
- `qc.csv`：基线资料，首行为 `qc_id,equipment,method,batch_scope,decision,checked_on`。

## 基线检查

运行 `python3 -m unittest discover -s tests -v` 可检查资料可读性、主键唯一性和版本锚点。该检查不实现业务分析能力。
