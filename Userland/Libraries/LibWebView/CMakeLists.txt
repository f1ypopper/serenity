set(SOURCES
    DOMTreeModel.cpp
    ImageDecoderClientAdapter.cpp
    OutOfProcessWebView.cpp
    RequestServerAdapter.cpp
    StylePropertiesModel.cpp
    WebContentClient.cpp
    WebSocketClientAdapter.cpp
)

set(GENERATED_SOURCES
    ../../Services/RequestServer/RequestClientEndpoint.h
    ../../Services/RequestServer/RequestServerEndpoint.h
    ../../Services/WebContent/WebContentClientEndpoint.h
    ../../Services/WebContent/WebContentServerEndpoint.h
)

serenity_lib(LibWebView webview)
target_link_libraries(LibWebView LibGfx LibGUI LibImageDecoderClient LibIPC LibProtocol LibWeb)

add_subdirectory(DumpLayoutTree)
