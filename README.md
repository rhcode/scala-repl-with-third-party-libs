#### scala repl with 3rd party libraries

To start run
```
sbt console
```

Some handy imports to start with
```
import akka.actor.ActorSystem
import akka.stream.{ActorMaterializer, ActorMaterializerSettings, Supervision}
import akka.stream.scaladsl.{Flow, Keep, Source, Sink}
import akka.util.Timeout
import scala.concurrent.duration._
import scala.util.{Failure, Success, Try}

implicit val system = ActorSystem("TestActorSystem")
implicit val executionContext = system.dispatcher
implicit val materializer = ActorMaterializer()
```
