Быстрый поиск в массиве
function quick_sort!(A)
if isempty(A)
return A
end
N = length(A)
K, M = part_sort!(A, A[rand(1:N)]) # - "базовый" элемент массива выбирается
случайным образом
quick_sort!(@view A[1:K])
quick_sort!(@view A[M:N])
return A
end
