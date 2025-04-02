# Unreal Documentation

## Debug

### Messaging
```C++
  
  /**
   * @param Key A unique key to prevent the same message from being added multiple
   *            times.
   * @param TimeToDisplay How long to display the message, in seconds.
   * @param DisplayColor The color to display the text in.
   * @param DebugMessage The message to display.
   * @param bNewerOnTop
   * @param TextScale
   */
  void AddOnScreenDebugMessage( uint64 Key, float TimeToDisplay, 

                                FColor DisplayColor, const FString& DebugMessage,
                                bool bNewerOnTop, const FVector2D& TextScale );

  
  // Example

  // Print string
  GEngine->AddOnScreenDebugMessage( -1, 5.f, FColor:: Green, "Message" );

  // Print string
  GEngine->AddOnScreenDebugMessage( -1, 5.f, FColor:: Green, "Message" ); 
  

```

#### float to String

```c++
  
  // Example
  float f = 0.1f;
  FString::SanitizeFloat( f );
  ```

### Drawing

```C++
  DrawDebugDirectionalArrow
  

```

## Math

### FQuat (Quaternion)
```C++
  
  /**
   * Creates and initializes a new quaternion from the a rotation around the given
   * axis.
   *
   * @param Axis assumed to be a normalized vector
   * @param Angle angle to rotate above the given axis (in radians)
   */
  TQuat( TVector< T > Axis, T AngleRad );
  
  // Example
  
  
  ```
