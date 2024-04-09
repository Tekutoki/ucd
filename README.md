### Use Case Diagram: Веб-додаток для бронювання готельних номерів

```plantuml
@startuml

left to right direction
skinparam usecase {
    BackgroundColor PaleGreen
    BorderColor DarkGreen
}

actor Користувач as User
actor Адміністратор as Admin

rectangle "Варіанти використання для Користувача" {
    usecase "Пошук готелів" as SearchHotels
    usecase "Перегляд деталей готелю" as ViewHotelDetails
    usecase "Бронювання номеру" as ReserveRoom
    usecase "Перегляд своїх бронювань" as ViewReservations
}

rectangle "Варіанти використання для Адміністратора" {
    usecase "Управління готелями" as ManageHotels
    usecase "Аналітика та звіти" as AnalyticsReports
}

rectangle "Загальні варіанти використання" {
    usecase "Реєстрація" as Registration
    usecase "Авторизація" as Authorization
}

User --> SearchHotels
User --> ViewHotelDetails
User --> ReserveRoom
User --> ViewReservations

Admin --> ManageHotels
Admin --> AnalyticsReports

@enduml
