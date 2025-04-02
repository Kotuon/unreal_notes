# Debug Tools

## Messaging

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

  // Print bool
  GEngine->AddOnScreenDebugMessage( -1, 5.f, FColor:: Green, 
                                  MyBool ? "true" : "false" );

  // Print int
  GEngine->AddOnScreenDebugMessage( -1, 5.f, FColor:: Green, 
                                  FString::FromInt( MyInt ) );

  // Print float
  GEngine->AddOnScreenDebugMessage( -1, 5.f, FColor:: Green, 
                                  FString::SanitizeFloat( MyFloat ) );

  

```

## Drawing

```C++

  //Example
  DrawDebugDirectionalArrow(
    GetWorld(), parent->GetActorLocation(),
    parent->GetActorLocation() + ( search_direction * Range ), 10.f,
    FColor::Green, false, 1.f, ( uint8 )0U, 2.f );

```
