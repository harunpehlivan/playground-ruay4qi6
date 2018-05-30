```C++ runnable
template<typename T>
class Wrapper
{
public:
    Wrapper(T const& value) : value_(value) {}
    
    T const& get() const { return value_; }
    
private:
    T value_;
};

int main()
{
    using IntWrapper = Wrapper<int>;
    int a = 42;
    IntWrapper intWrapper(a);
    
    intWrapper.get() = 43;
}
```

