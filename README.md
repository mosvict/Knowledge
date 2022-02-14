## Knowledge (Ruby on Rails)

- Replace 4 last characters to '*'
```
string.replace(/.(?=.{4,}$)/g, ‘*’)
```

- Router with devise
```
devise_scope :user do
  authenticated :user do
    root 'home#index', as: :authenticated_root
  end

  unauthenticated do
    root 'devise/sessions#new', as: :unauthenticated_root
  end
end
```
