# PSNR(Peak Signal-to-noise ratio)
* 최대 신호에서 잡음비
* 8bit gray-scale에서 최대 신호 = 255 -> 8bit로 나타낸 이미지의 최대 신호 => 255에 대한 noise 비율
* 영상 또는 영상 압축에서 화질의 손실 정보를 평가할 때 사용한다.
* 화질 손실이 적으면 적을 수록 PSNR의 값은 커진다.
* $`PSNR = 10 * \log_{10} \left( \frac{MAX(IMAGE)^2}{MSE} \right)`$
* MSE = Mean Square Error
