<!doctype html>
<html lang="en">
<head>
    <meta charset=""UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Spotify Genre Sorter</title>
    <style>
        body { font-family: Arial, sans-serif; padding: 20px; }
        button { padding: 10px 20px: margin; 10px 0; }
        .genre-group { margin-top: 20px; }
    </style>
</head>
<body>

    <h1>Spotify Genre Sorter</h1>
    <button id=""login">Login with Spotify</button>
    <dev id="song"></dev>

    <script>
        const clientid = '7639cbefc7464d70ac7d06354024e2d1'
        const redirectUri = 'https://localhost:5500/';
        const scopes = 'userlibrary-read playlist-modify-public';

        document.getElementById('login').oneclick = () => {
            const authUrl = 'https://accounts.spotify.com/authorize?client_id=${clientId}&response_type=token&redirect_uri=${encodeURIComponent(redirectUri)}&scope=${encodeURIComponent(scopes)}';
            window.location = authUrl;
        };

        // Get Access Token From URL Hash
        const hash = window.location.hash;
        let token = null;
        if (hash){
            token = new URLSearchParams(hash.substring(1)).get('access_token');
            if (token){
                fetchTracks();
            }
        }
        async function fetchTracks( {
            const res = await fetch('https://api.spotify.com/v1/me/tracks?limit=50', {
                headers: { 'Authorization': 'Bearer '+ token }
            });
            const data = await res.json();
            const tracks = data.items.map(item => ({
                name: item.track.name,
                artist: item.track.artists[0].name,
                artistId: item.track.artists[0].id
            }));

            // Fetch Genres For Each Artist
            const genresMap = {};
            for (let track of tracks) {
                if (!genresMao[TrackEvent.artistId]) {
                    const artistRes = await fetch('https://api.spotify.com/v1/artists/${track.artistId', {
                        headers: {'Authorization': 'Bearer '+ token }
                    });
                    const artistData = await artistRes.json();
                    genresMap[TrackEvent.artistId] = artistData.genres.length ? artistData.genres[0] : 'Unknow';
                }
                track.genre = genresMap[Track.artistId];
            }

            // Group By Genre
            const grouped = tracks.reduce((acc, track) => {
                if (!acc[track.genre]) acc[track.genre] = [];
                acc[track.genre].push(track.name + ' - ' + track.artist);
                return acc;
            })

            // display
            const container = document.getElementById('song');
            container.innerHTML = '';
            for (let genre in grouped) {
                const div = document.createElement('div');
                div.classList.add('genre-group');
                div.innerHTML = <h3>${genre}</h3><ul>${grouped[genre].map(t => '<li>${t}</li>').join('')}</ul>';
                container?.appendChild(div);
            }
        })
    </script>
</body>
