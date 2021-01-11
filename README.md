# Reinforcement-Learning - Link video : https://youtu.be/mhNjxRYvDTw
1.
Viết tác nhân lặp giá trị vào ValueIterationAgent, tác nhân này đã được chỉ định một phần trong valueIterationAgents.py. Tác nhân lặp lại giá trị của bạn là một công cụ lập kế hoạch ngoại tuyến, không phải một tác nhân học tập củng cố và do đó, tùy chọn đào tạo có liên quan là số lần lặp lại giá trị mà nó sẽ chạy (tùy chọn -i) trong giai đoạn lập kế hoạch ban đầu. ValueIterationAgent lấy MDP khi xây dựng và chạy lặp giá trị cho số lần lặp được chỉ định trước khi hàm tạo trả về.
2.
 Thay đổi 1 trong các thông số chiết khấu và độ ồn sao cho chính sách tối ưu khiến đại lý nỗ lực qua cầu. Đặt câu trả lời trong question2()các analysis.py
3.
Xem xét bố cục DiscountGrid, được hiển thị bên dưới. Lưới này có hai trạng thái đầu cuối với mức hoàn trả dương (ở hàng giữa), điểm thoát gần với điểm hoàn vốn +1 và điểm thoát xa với điểm hoàn vốn +10. Hàng dưới cùng của lưới bao gồm các trạng thái đầu cuối có phần thưởng âm (được hiển thị bằng màu đỏ); mỗi tiểu bang trong khu vực "vách đá" này có điểm thưởng -10. Trạng thái bắt đầu là hình vuông màu vàng. Chúng tôi phân biệt giữa hai loại đường đi: (1) đường đi "mạo hiểm vách đá" và đi gần hàng dưới cùng của lưới; những con đường này ngắn hơn nhưng có nguy cơ kiếm được khoản hoàn trả âm lớn và được thể hiện bằng mũi tên màu đỏ trong hình bên dưới. (2) đường đi "tránh vách đá" và đi dọc theo mép trên của lưới. Những con đường này dài hơn nhưng ít có khả năng phải chịu các khoản hoàn trả âm rất lớn.
4.
Viết một Q-learning agent, nó thực hiện rất ít trong việc xây dựng, mà thay vào đó học bằng cách thử và sai từ các tương tác với môi trường thông qua phương pháp update(state, action, nextState, reward) của nó . Một sơ khai của một Q-học được quy định tại QLearningAgenttrong qlearningAgents.py, và bạn có thể chọn nó với các tùy chọn '-a q'. Đối với câu hỏi này, bạn phải thực hiện update, computeValueFromQValues, getQValue, và computeActionFromQValuesphương pháp.
5.
Hoàn thành tác nhân Q-learning của bạn bằng cách triển khai lựa chọn hành động tham lam epsilon getAction, nghĩa là nó chọn các hành động ngẫu nhiên trong một phần thời gian epsilon và theo cách khác, giá trị Q tốt nhất hiện tại của nó. Lưu ý rằng việc chọn một hành động ngẫu nhiên có thể dẫn đến việc chọn một hành động tốt nhất - nghĩa là bạn không nên chọn một hành động tối ưu phụ ngẫu nhiên mà nên chọn bất kỳ hành động pháp lý ngẫu nhiên nào.
6.
Đầu tiên, đào tạo một Q-learning hoàn toàn ngẫu nhiên với tốc độ học mặc định trên BridgeGrid không ồn ào trong 50 tập và quan sát xem nó có tìm ra chính sách tối ưu hay không.

8.
Triển khai một tác nhân Q-learning gần đúng để tìm hiểu trọng số cho các tính năng của các trạng thái, trong đó nhiều trạng thái có thể chia sẻ các tính năng giống nhau. Viết  lớp ApproximateQAgent -  qlearningAgents.py, là lớp con của PacmanQAgent.
