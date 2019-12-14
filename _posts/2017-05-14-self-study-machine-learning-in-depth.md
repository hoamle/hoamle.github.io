---
title: "Tự học Machine Learning chuyên sâu"
layout: post
category: machine learning
---
Trong bài viết này, mình muốn chia sẻ:
* (A) ***[a Map of Machine Learning](#map)*** - bản đồ khái quát bức tranh toàn thể của các mảng lớn trong Machine Learning và Deep Learning (ML/DL); và *quan trọng hơn* là 
* (B) ***kinh nghiệm TỰ HỌC/nghiên cứu*** để nắm được bức tranh toàn cảnh đó, từ đấy tìm được những giải pháp tối ưu cho công việc/dự án riêng. 

> (Những chia sẻ dưới đây rút ra từ quá trình học và làm việc của bản thân. Trong đó có 2+ năm tự học/làm việc tập trung về ML/AI + training cho các thành viên trong DSLab-HUST. Vì thế sẽ có selection bias và một số điểm cần cải thiện, bổ sung, nên rất hi vọng có thêm những ý kiến trao đổi & đóng góp từ mọi người!)

---

## A. A Map of Machine Learning
Lợi ích lớn nhất của việc có cái nhìn rộng và bao quát hơn về ML/AI, đó là (i) tránh để bị lạc trong *bạt ngàn* những mô hình/phương pháp/tài liệu đã và đang sinh sôi ngày càng nhiều trong đợt sóng AI lần thứ 3 này; (ii) tránh được những kỳ vọng không thực tế (do uninformed hype!) khi đi tìm giải pháp ML/AI cho bài toán của mình, cũng như (iii) hiểu pipeline/độ phù hợp/ưu nhược của các giải pháp/mô hình với bài toán, và (iv) technical details trong [các ứng dụng thú vị [1]](#ref).

Chắc hẳn có rất nhiều bạn như mình, đến với ML/AI buổi ban đầu qua việc tự học các online course và tutorial, và có những lúc *ngợp* trước một "rừng" các mô hình/kỹ thuật ML/DL/AI [[2]](#ref) ra đời hàng *tuần*, cũng như một rừng các tài liệu ML/AI liên quan [[3]](#ref). Đó là còn chưa kể đến các công việc thuộc những mảng trọng tâm khác trong ngành, vd. phương pháp học mô hình (inference methods), hay những vấn đề nảy sinh khi huấn luyện mô hình theo Generative Adversarial Networks (GAN) framework ... , cùng hàng đống khái niệm rất hay nghe tên nhưng lại tù mù không biết chúng là gì và làm gì.

Tuy nhiên, dù rất nhiều, các mô hình trong ML/DL thực chất đều có thể phân loại vào MỘT SỐ ÍT *lớp mô hình (**model classes**)* tiêu biểu, và các khái niệm đều thuộc ~10 *khái niệm cốt lõi ([**core concepts**](https://hoamle.github.io/articles/16/essence-machine-deep-learning/#core))* mà bất kỳ mô hình ML nào cũng cần phải giải quyết. Cùng với đó, nếu có nền tảng bài bản về **xây dựng mô hình xác suất (probabilistic modelling)**, và kèm theo là **các phương pháp suy diễn Bayesian (Bayesian inference methods)**, ta cũng sẽ nắm được những chi tiết mấu chốt của gần như TOÀN BỘ các mô hình ML/DL - vd. mô hình làm gì, phù hợp với dữ liệu ntn, có những mô hình nào giải quyết vấn đề tương tự - và bức tranh toàn cảnh các vấn đề được quan tâm trong ML/DL{% sidenote 'sn-id-allmodels' 'Một số vấn đề đặc thù của DL, chủ yếu là của DNN, mà với chỉ nền tảng probabilistic modelling và Bayesian inference methods thì (có thể) chưa bao quát được hết, vd. \"*Thiết kế kiến trúc mạng (Architecture)*\"; hoặc cần kiến thức nền tảng sâu hơn về Toán/Lý, vd. \"*Ổn định quá trình tối ưu (minimax.) hàm mục tiêu của GAN-like models*\".' %}. 

> <a name="map">A map of ML</a>: Chi tiết về các node chính trên bản đồ cũng như các từ viết tắt được trình bày tại một [bài viết](https://hoamle.github.io/articles/16/essence-machine-deep-learning/#map) khác, và phần [study-plan](https://hoamle.github.io/articles/16/essence-machine-deep-learning/#plan) của bài viết.
{% maincolumn 'assets/img/mapofML.png' "" %}


## B. Kinh nghiệm tự học/nghiên cứu 
Như có đề cập ở trên, có nền tảng vững về *probabilistic modelling* và *Bayesian inference methods* là một trong những điều kiện cần để nắm được bức tranh toàn cảnh, và có thể đi xa hơn trong ML. Thực ra, quan trọng nhất vẫn là (B1) **học/tìm hiểu như thế nào cho đúng**, rồi mới đến (B2) **học/tìm hiểu cái gì** ("cái gì" trong bài này là probabilistic modelling và Bayesian inference methods).

### B1. Tips cho việc tự học/tìm hiểu nói chung
1. Minh họa các khái niệm/chủ đề mới bằng note viết tay, hình vẽ, code, ...
2. Học/làm có nhóm (cùng chung mục tiêu), online hay offline không quan trọng nếu có thời gian biểu rõ ràng. Lợi ích: (i) có nhiều thứ người khác biết mà mình không biết; (ii) dạy/hướng dẫn lại các khái niệm/chủ đề cho người khác một cách dễ hiểu là một cách tự học hiệu quả; (iii) "muốn đi nhanh thì đi một mình, muốn đi xa thì cần một đội" (vì đường dài luôn gian nan).
3. Cố gắng tiếp cận vấn đề rộng hơn một chút, vd. bằng các câu hỏi "for what?", "why", "why not Z"? 
4. Nếu có thể, hãy làm một (mini-)project liên quan nhất đến thứ mình muốn học, vì có thể học được rất nhiều thứ khác từ project. TUY NHIÊN, điều kiện cần là có người đi trước/expert chỉ dẫn; hoặc có kiến thức nền tảng vững; hoặc có cái nhìn bao quát nhưng cũng đủ chi tiết về project mình định theo đuổi. LÝ DO: Project nghe càng thú vị, càng có khả năng cao là phức tạp hơn nhiều so với những gì ta nghĩ ban đầu.
5. Với ML nói riêng, [Metacademy](https://metacademy.org) là một nguồn rất tốt để tìm hiểu một số khái niệm mới. Ưu điểm lớn nhất của trang là đưa ra *cụ thể* phần/mục nào trong tài liệu tham khảo các bạn cần đọc, và kiến thức nền tảng cần có là gì. Vd [https://metacademy.org/graphs/concepts/recurrent_neural_networks](https://metacademy.org/graphs/concepts/recurrent_neural_networks)
Ngoài ra còn có những gợi ý xây dựng lộ trình tự học ([study-plan/roadmap](https://metacademy.org/roadmaps/)) các chủ đề chuyên sâu trong ML để level-up.

### B2. Học probabilistic modelling cho "đúng"
Mục tiêu cần đạt là có **kiến thức "bài bản" về xây dựng mô hình ML bằng ngôn ngữ của probabilistic models** (ứng với `base` node + một phần `PGM` trong [bản đồ ML](#map) ở phần A). 

Tuy nhiên, học/tìm hiểu probabilistic models sao cho "có bài bản" lại tương đối thử thách, kể cả với những người đã có kiến thức thiết yếu/ kinh nghiệm làm ML. Lý do chính? LƯỢNG + ĐỘ SÂU kiến thức cần tiếp thu nhiều hơn NHIỀU so với vd. học/tìm hiểu các mô hình mạng nơ-ron sâu - DNN{% sidenote 'sn-id-challenge' 'Nhận định rút ra từ các thành viên trong DSLab-HUST, bản thân và các học viên trong lớp khi mình học Thạc sỹ về Computational Biology - một ngành dùng ML (và nhiều giải pháp khác) làm công cụ để giải quyết bài toán sinh học.' %}. Giải pháp? Cần "base" đủ vững. 

Rất tiếc là dù hiện tại có vô vàn online course/tutorial nhập môn ML/DNN, nhưng tài liệu tương tự - giới thiệu "bài bản" ML bằng ngôn ngữ của probabilistic models - lại không có/rất khó tìm{% sidenote 'sn-id-pgmcourse' 'Mình biết Coursera có [khóa học rất hay về probabilistic models](https://www.coursera.org/specializations/probabilistic-graphical-models) của GS Daphne Koller. TUY NHIÊN khóa học không tập trung vào ML, tương đối rộng và sâu, nên RẤT CẦN có kiến thức *bài bản* về xây dựng mô hình ML trước khi học. Nếu ai biết tài liệu nào phù hợp hơn thì tốt quá.' %}. 

Nhưng như thế nào là "bài bản"? Mình vốn đang viết một tutorial chi tiết gồm 4 phần để làm việc này nhưng chưa có thời gian hoàn thiện, nên hiện tại tạm thời lược qua các ý chính sau:
- nắm được quy trình phân tích dữ liệu - (statistical) data analysis, 
- định nghĩa được tường minh (có thể đo đạc/tính toán) các bước trong quy trình
- hệ thống hóa được những kiến thức về xây dựng mô hình ML, vd. như [https://hoamle.github.io/articles/16/essence-machine-deep-learning/#core](https://hoamle.github.io/articles/16/essence-machine-deep-learning/#core) + PART 1a trong mục [Course notes](https://hoamle.github.io/articles/16/essence-machine-deep-learning/#note).
- quy được các mô hình/thuật toán ML/DL phổ biến về probabilistic models + inference methods tương ứng (nếu có thể).

Trên đây là những kinh nghiệm của bản thân mình. Hi vọng có ích và nhận được những ý kiến trao đổi & đóng góp từ mọi người.

## <a name="ref">References</a>
1. Tham khảo các threads trên reddit's [r/machinelearning](https://www.reddit.com/r/MachineLearning), creativeai.net, kênh [Two-minute Papers](https://www.youtube.com/user/keeroyz) trên youtube; chia sẻ (chủ yếu qua Twitter) và bài viết của các nhân vật tiêu biểu trong ngành, ...
1. ["Neural Nets Zoo"](http://www.asimovinstitute.org/neural-network-zoo/), ["The GAN Zoo"](https://deephunt.in/the-gan-zoo-79597dc8c347), các mô hình trong [bản đồ ML](#map) ở phần A, và còn nhiều nữa.
1. Các MOOCs trên Coursera, EdX, Udacity, Udemy. Các danh sách tổng hợp, vd. của [deeplearning.net (MILA)](http://deeplearning.net/reading-list/), ["Awesome Deep Vision"](https://github.com/kjw0612/awesome-deep-vision), ...
