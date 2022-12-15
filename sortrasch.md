Сортировка расчесыванием
function comb_sort!(A)
g = length(A)
sorted = false
sm=0
while !sorted
g /= 1.237
if g < 1
g = 1
sorted = true
end
swapped = false
for i in 1:length(A)-floor(Int, g)
sm = floor(Int, g) + i
if A[i] > A[sm]
A[i], A[sm] = A[sm], A[i]
swapped = false
end
end
end
end
f(x) = x
