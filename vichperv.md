# Вычисление первых k порядковых статистик O(N) (k ститать фиксированным и много меньшим N)
function order_statistics!(A, i)
N = length(A)
b = A[rand(1:N)]
K, M = part_sort!(A, b)
if K < i < M
return A[i]
elseif i <= K
return order_statistics!(@view(A[1:K]), i)
else # i >= M
return order_statistics!(@view(A[M:N]), i)
end
end
order_statistics(A, i) = order_statistics!(copy(A), i)
