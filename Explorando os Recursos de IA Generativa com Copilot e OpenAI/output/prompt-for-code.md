public class Sudoku {
    private static final int SIZE = 9;
    private static int[][] board = {
        {5, 3, 0, 0, 7, 0, 0, 0, 0},
        {6, 0, 0, 1, 9, 5, 0, 0, 0},
        {0, 9, 8, 0, 0, 0, 0, 6, 0},
        {8, 0, 0, 0, 6, 0, 0, 0, 3},
        {4, 0, 0, 8, 0, 3, 0, 0, 1},
        {7, 0, 0, 0, 2, 0, 0, 0, 6},
        {0, 6, 0, 0, 0, 0, 2, 8, 0},
        {0, 0, 0, 4, 1, 9, 0, 0, 5},
        {0, 0, 0, 0, 8, 0, 0, 7, 9}
    };

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        printBoard();
        
        while (true) {
            System.out.println("Digite linha (1-9), coluna (1-9) e número (1-9) separados por espaço:");
            int row = scanner.nextInt() - 1;
            int col = scanner.nextInt() - 1;
            int num = scanner.nextInt();
            
            if (isValidMove(row, col, num)) {
                board[row][col] = num;
                printBoard();
            } else {
                System.out.println("Movimento inválido! Tente novamente.");
            }
        }
    }

    private static boolean isValidMove(int row, int col, int num) {
        for (int i = 0; i < SIZE; i++) {
            if (board[row][i] == num || board[i][col] == num) {
                return false;
            }
        }
        
        int boxRow = row - row % 3;
        int boxCol = col - col % 3;
        
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                if (board[boxRow + i][boxCol + j] == num) {
                    return false;
                }
            }
        }
        
        return true;
    }

    private static void printBoard() {
        System.out.println("Tabuleiro Sudoku:");
        for (int i = 0; i < SIZE; i++) {
            for (int j = 0; j < SIZE; j++) {
                System.out.print((board[i][j] == 0 ? "." : board[i][j]) + " ");
            }
            System.out.println();
        }
    }
}
