import java.util.*;

class Movie {
    String title;
    String rating;
    double score;

    public Movie(String title, String rating, double score) {
        this.title = title;
        this.rating = rating;
        this.score = score;
    }

    public String getRating() {
        return rating;
    }

    public double getScore() {
        return score;
    }
}

public class MovieRatingsAnalyzer {
    public static void main(String[] args) {
        List<Movie> movies = new ArrayList<>();
        movies.add(new Movie("Movie1", "PG", 4.5));
        movies.add(new Movie("Movie2", "PG-13", 3.8));
        movies.add(new Movie("Movie3", "R", 4.2));
        movies.add(new Movie("Movie4", "PG-13", 4.0));
        movies.add(new Movie("Movie5", "PG", 3.9));

        Map<String, Integer> ratingCounts = new HashMap<>();
        Map<String, Double> ratingAverages = new HashMap<>();

        for (Movie movie : movies) {
            String rating = movie.getRating();
            double score = movie.getScore();

            if (!ratingCounts.containsKey(rating)) {
                ratingCounts.put(rating, 1);
                ratingAverages.put(rating, score);
            } else {
                ratingCounts.put(rating, ratingCounts.get(rating) + 1);
                ratingAverages.put(rating, ratingAverages.get(rating) + score);
            }
        }

        for (String rating : ratingCounts.keySet()) {
            int count = ratingCounts.get(rating);
            double average = ratingAverages.get(rating) / count;
            System.out.println("Rating: " + rating + ", Number of Movies: " + count + ", Average Rating: " + average);
        }
    }
}
