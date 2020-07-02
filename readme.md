# Youtube GameBar Search Server
A simple server to implement YTGBO's Search feature, using node-ytsr library.

## Usage
* 1: Clone this repository.  
* 2: On repository's root, run `npm install`.  
* 3: To run the server, use: `node index.js`.  
* 4: Make any request to the server:
  * 4.1: A POST request on `http://server.address:54522/search/` with the following body is accepted:
    * 4.1.1: `{ "term": "your_search_term_here" }`.  
  * 4.2: A GET request with the following URL parameter is accepted:
    * 4.2.1: `http://server.address:54522/search/your_search_term_here`
* 5: If the search was successful, server will return an `Object[]`:
  * 5.1: Each `object` has these attributes: 
    ```
    {
      "mediaTitle": "the_search_result_video/playlist_title",
      "channelTitle": "the_search_result_channel_title",
      "mediaUrl": "the_search_result_video/playlist_url"
    }
    ```

## Tips
It is highly recommended to use the `pm2` process manager to recover from internal failures and automatize the service providing.

## Special Thanks
[Guilhermeasper](https://github.com/guilhermeasper) for implementing playlists search capability.

## Licensing
MIT License.
