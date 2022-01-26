class Solution:
    def findDiagonalOrder(self, mat: List[List[int]]) -> List[int]:
        x = -1
        y = 1
        i = 1
        j = -1
        counts = list()
        merge_right = len(mat[0])
        merge_bottom = len(mat)
        while mat:
            if merge_bottom == 1:
                for _ in range(merge_right):
                    counts.append(mat[0][_])
                return counts
            if merge_right == 1:
                for _ in range(merge_bottom):
                    counts.append(mat[_][0])
                return counts
            if (i+x < 0 or i+x >= merge_bottom or i == merge_bottom) and j != merge_right-1:
                x = -x
                y = -y
                j += 1
                if len(counts) == merge_right*merge_bottom:
                    return counts
                counts.append(mat[i][j])
            elif (j+y < 0 or j+y >= merge_right or j == merge_right) and i != merge_bottom-1:
                x = -x
                y = -y
                i += 1
                if len(counts) == merge_right*merge_bottom:
                    return counts
                counts.append(mat[i][j])
            j = j + y
            i = i + x
            if len(counts) == merge_right*merge_bottom:
                return counts
            counts.append(mat[i][j])
