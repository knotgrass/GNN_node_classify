## GNN_introduction

## TODO
task: tạo graph
yêu cầu,
tạo node: mỗi bnb là 1 box, node feature =  phoBERT(word sau khi orc, có thể dùng có dấu hoặc ko dấu) concat tọa độ box(dùng format yolo vì đẫ normalize)
tạo edge: sắp xếp các box trong 1 dòng theo thứ tự x tăng dần (từ trái qua phải)
cạnh sẽ nối 2 node cạnh nhau (hoặc tất cả các node trong cùng 1 dòng đều nối nhau), chỉ tồn tại edge nối 2 node trong cùng 1 dòng

## problem
1. deal with unbalance node
* tạo lại graph , giới hạn số lượng node, rồi gen ra graph sau
* focal loss 

### inference
* tạo graph, kết hợp `dkkd_create_graph.py` và  `DkkdGraphDataset.__getitem__`
* cần sửa 
### requirement
* https://pytorch.org/get-started/locally/
* https://www.dgl.ai/
* https://github.com/pbcquoc/vietocr
* https://github.com/VinAIResearch/PhoBERT

