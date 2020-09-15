<h1>Sandbox</h1>

Sandbox is a simple 2D engine to build every possible 2D game you can think of.
It is a library, so you use it in java code to build your game with it.
It uses the LWJGL library which uses the OpenGL Api to render.

It is planned to create a engine - ui - editor, so you don't need to know how to code.

<h3>Examples</h3>

<h5>\[Simple App example\]</h5>
````
//imports ...

public class MyGame extends SandboxApp {

    public static final String SCENE_MAIN = "mainScene";
    private static final double SCENE_MAIN_GRAVITY = 0.8;

    @Override
    public SceneManager init(SceneManager manager){
        Scene mainScene = manager.createScene();
        SceneEnvironment environment = new BasicPlatformerEnvironment(SCENE_MAIN_GRAVITY);
        mainScene.setEnvironment(environment);

        manager.registerScene(SCENE_MAIN, mainScene);
        manager.setInitialScene(SCENE_MAIN);

        return manager;
    }

    public static void main(String[] args){
        Sandbox.run(MyGame.class);
    }

}
````
