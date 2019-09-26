# Music Meteorologist Data Science API

This Flask app takes in the ID of a Spotify song from an HTTP POST request and outputs three recommended songs (specifically their IDs and cosine similarity scores).

Once the Flask app has received a request, it calls the Spotify API to retrieve the characteristics of the Spotify song and converts those characteristics to a NumPy array. Then, the function all_similarities() is called, where a is the numpy array of the song characteristics and dfy is a component of our database of songs (to which this Spotify song will be compared, and from where we will receive our predictions).

/*def cosine_similarity(a, b):
  dot_product = np.dot(a,b)
  norm_a = np.linalg.norm(a)
  norm_b = np.linalg.norm(b)
  return dot_product / (norm_a * norm_b)
  #return np.sqrt(np.sum((a - b) ** 2))
def all_similarities(a, dfy):
  similar_songs = []
  for spotify_song, metadata in zip(array, dfy.values):
    similarity = cosine_similarity(a, spotify_song)
    similar_songs.append({'similarity': ''.join(str(similarity.tolist())), 'values': metadata[1]})
  return similar_songs*/
