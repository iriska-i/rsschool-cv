# Yelyzaveta Holovatiuk

Computer Science student / learning to code

## Contact

- Email: mango.mango14uuu@gmail.com
- GitHub: [github.com/iriska-i](https://github.com/iriska-i)
- Discord: iriska_01044
- Location: Poland

## About

I'm studying Software Engineering at the University of Information Technology and Management in Rzeszów since October 2023. Before that I finished a high school specializing in new information technologies, along with Cisco Networking Academy courses (CCNA and Linux Essentials). I'm currently learning Python, C#, and JavaScript, including through the RS School course. Looking for a first professional experience - an internship, apprenticeship, or a project where I can actually learn by doing.

## Skills

- Programming languages: Python, C#, JavaScript (basic level)
- Databases: PostgreSQL
- Tools & environments: Git, Visual Studio, VS Code, GitHub
- Methodologies: Agile / Scrum

## Code example

BFS pathfinding solver from a maze-generator project — finds the shortest
path through a randomly generated maze stored as a grid, using a queue-based
breadth-first search.

```python
class SolverBFS(BazowySolver):
    def rozwiaz(self, siatka, start, koniec):
        kolejka = deque()
        kolejka.append((start, [start]))
        odwiedzone = set()
        odwiedzone.add(start)

        while kolejka:
            (wiersz, kol), sciezka = kolejka.popleft()
            if (wiersz, kol) == koniec:
                return sciezka
            for dw, dk in [(-1, 0), (1, 0), (0, -1), (0, 1)]:
                nw, nk = wiersz + dw, kol + dk
                if (0 <= nw < len(siatka) and
                        0 <= nk < len(siatka[0]) and
                        siatka[nw][nk] == 0 and
                        (nw, nk) not in odwiedzone):
                    odwiedzone.add((nw, nk))
                    kolejka.append(((nw, nk), sciezka + [(nw, nk)]))
        return []
```

## Education

- **05.2023** — High School of New Information Technologies (secondary education)
- **10.2023 – present** — University of Information Technology and Management in Rzeszów — Software Engineering (Engineer's degree)

## Certificates

- CCNA: Introduction to Networks / Switching, Routing, and Wireless Essentials — Cisco Networking Academy
- NDG Linux Essentials / Linux Unhatched — Cisco Networking Academy & Network Development Group