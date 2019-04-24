---
title: Controlar valores altos y ajuste de PPP en una solución de Office
description: Actualizar una solución de Office, como los paneles de tareas personalizados o los controles ActiveX, para admitir monitores con un valor alto de PPP.
ms.date: 03/09/2019
localization_priority: Normal
ms.openlocfilehash: 0425e5e9dd0f060a6336888cfe6c236b39732080
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301760"
---
# <a name="handle-high-dpi-and-dpi-scaling-in-your-office-solution"></a><span data-ttu-id="aa092-103">Controlar valores altos y ajuste de PPP en una solución de Office</span><span class="sxs-lookup"><span data-stu-id="aa092-103">Handle high DPI and DPI scaling in your Office solution</span></span>

<span data-ttu-id="aa092-104">Muchas configuraciones de equipo y pantalla ahora admiten resoluciones con un valor alto de PPP (puntos por pulgada) y pueden conectar varios monitores de diferentes tamaños y densidad de píxeles.</span><span class="sxs-lookup"><span data-stu-id="aa092-104">Many computer and display configurations now support high DPI (dots-per-inch) resolutions, and can connect multiple monitors with different sizes and pixel densities.</span></span> <span data-ttu-id="aa092-105">Esto requiere aplicaciones para ajustar cuando el usuario mueve la aplicación a un monitor con un valor de PPP diferente o cambia el nivel de zoom.</span><span class="sxs-lookup"><span data-stu-id="aa092-105">This requires applications to adjust when the user moves the app to a monitor with a different DPI, or changes the zoom level.</span></span> <span data-ttu-id="aa092-106">Aplicaciones que no son compatibles con el ajuste de PPP se podrían ver bien en monitores con bajos valores de PPP, pero se verán expandidas y borrosas cuando se muestran en un monitor con un valor alto de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-106">Applications that don’t support DPI scaling might look fine on low DPI monitors, but will look stretched and blurry when shown on a high DPI monitor.</span></span> 

<span data-ttu-id="aa092-107">Se han actualizado las aplicaciones de Office 2016, como Word y Excel, para responder a los cambios en el factor de escala.</span><span class="sxs-lookup"><span data-stu-id="aa092-107">Office 2016 applications, such as Word and Excel, have been updated to respond to changes in scale factor.</span></span> <span data-ttu-id="aa092-108">Sin embargo, la solución de Office también debe responder a cambios para dibujar correctamente cuando cambie el valor de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-108">However, your Office solution must also respond to changes to draw correctly when the DPI changes.</span></span> <span data-ttu-id="aa092-109">Este artículo describe cómo admite Office PPP dinámicos y qué puede hacer para garantizar la mejor experiencia visual de la solución de extensibilidad de Office para controlar el ajuste de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-109">This article describes how Office supports dynamic DPI, and what steps you can take to ensure the best viewing experience for your Office extensibility solution to handle DPI scaling.</span></span> 

## <a name="dpi-scaling-symptoms-in-your-solution"></a><span data-ttu-id="aa092-110">Síntomas de ajuste de PPP en su solución</span><span class="sxs-lookup"><span data-stu-id="aa092-110">DPI scaling symptoms in your solution</span></span>

<span data-ttu-id="aa092-111">Windows aplica el ajuste de PPP cuando una aplicación se mueve de una pantalla a otra con un valor de PPP diferente.</span><span class="sxs-lookup"><span data-stu-id="aa092-111">Windows applies DPI scaling when an application is moved from one display to another display with a different DPI.</span></span> <span data-ttu-id="aa092-112">Esto ocurre en casos como arrastrar una aplicación a un monitor diferente o acoplar un portátil.</span><span class="sxs-lookup"><span data-stu-id="aa092-112">This happens in scenarios such as dragging an application to a different monitor or docking your laptop.</span></span> <span data-ttu-id="aa092-113">Si el ajuste de PPP afecta negativamente a la solución de Office, verá uno o varios de los síntomas siguientes:</span><span class="sxs-lookup"><span data-stu-id="aa092-113">If your Office solution is adversely affected by DPI scaling, you will see one or more of the following symptoms:</span></span>

- <span data-ttu-id="aa092-114">Las ventanas se dibujan en una ubicación incorrecta o tiene un tamaño incorrecto.</span><span class="sxs-lookup"><span data-stu-id="aa092-114">The windows draw in the wrong location or have incorrect sizing.</span></span>
- <span data-ttu-id="aa092-115">Elementos como botones y etiquetas aparecen en una ubicación incorrecta en la ventana de su solución.</span><span class="sxs-lookup"><span data-stu-id="aa092-115">Elements such as buttons and labels appear in the wrong location in your solution’s window.</span></span>
- <span data-ttu-id="aa092-116">Fuentes e imágenes aparecen demasiado grandes, demasiado pequeñas o en una ubicación incorrecta.</span><span class="sxs-lookup"><span data-stu-id="aa092-116">Fonts and images appear too small, too large or in the wrong location.</span></span>

<span data-ttu-id="aa092-117">Los siguientes tipos de soluciones de Office se pueden ver afectados por el ajuste de PPP:</span><span class="sxs-lookup"><span data-stu-id="aa092-117">The following types of Office solutions can be affected by DPI scaling:</span></span>

- <span data-ttu-id="aa092-118">Complementos VSTO</span><span class="sxs-lookup"><span data-stu-id="aa092-118">VSTO Add-ins</span></span>
- <span data-ttu-id="aa092-119">Paneles de tareas personalizados</span><span class="sxs-lookup"><span data-stu-id="aa092-119">Custom task panes</span></span>
- <span data-ttu-id="aa092-120">Complementos COM</span><span class="sxs-lookup"><span data-stu-id="aa092-120">COM Add-ins</span></span>
- <span data-ttu-id="aa092-121">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="aa092-121">ActiveX controls</span></span>
- <span data-ttu-id="aa092-122">Extensiones de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="aa092-122">Ribbon extensions</span></span>
- <span data-ttu-id="aa092-123">Servidores OLE</span><span class="sxs-lookup"><span data-stu-id="aa092-123">Ole servers</span></span>
- <span data-ttu-id="aa092-124">Complementos web de Office</span><span class="sxs-lookup"><span data-stu-id="aa092-124">Office web add-ins</span></span>

## <a name="windows-dpi-awareness-modes"></a><span data-ttu-id="aa092-125">Modos de reconocimiento de PPP de Windows</span><span class="sxs-lookup"><span data-stu-id="aa092-125">Windows DPI awareness modes</span></span>

<span data-ttu-id="aa092-126">En este artículo haremos referencia a los modos de reconocimiento de PPP compatibles con Windows.</span><span class="sxs-lookup"><span data-stu-id="aa092-126">Throughout this article we’ll refer to the DPI awareness modes that Windows supports.</span></span> <span data-ttu-id="aa092-127">Cada modo de reconocimiento de PPP es compatible con distintas funciones, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="aa092-127">Each DPI awareness mode supports different capabilities, as described in the following table.</span></span> <span data-ttu-id="aa092-128">Esta es una descripción simplificada de los modos para explicar cómo las soluciones de Office son compatibles.</span><span class="sxs-lookup"><span data-stu-id="aa092-128">This is a simplified description of the modes to explain how Office solutions support them.</span></span> <span data-ttu-id="aa092-129">Para obtener más información sobre los modos de reconocimiento de PPP, vea [Desarrollo de aplicaciones de escritorio con un valor alto de PPP en Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).</span><span class="sxs-lookup"><span data-stu-id="aa092-129">For more information about the DPI awareness modes, see [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).</span></span>

|<span data-ttu-id="aa092-130">Modo</span><span class="sxs-lookup"><span data-stu-id="aa092-130">Mode</span></span>  |<span data-ttu-id="aa092-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa092-131">Description</span></span>  |<span data-ttu-id="aa092-132">Cuando cambia PPP</span><span class="sxs-lookup"><span data-stu-id="aa092-132">When DPI changes</span></span>  |
|---------|---------|---------|
|<span data-ttu-id="aa092-133">Sin reconocimiento de PPP</span><span class="sxs-lookup"><span data-stu-id="aa092-133">DPI unaware</span></span> |  <span data-ttu-id="aa092-134">La aplicación siempre se representa como si se encontrara en una pantalla con un valor de PPP de 96.</span><span class="sxs-lookup"><span data-stu-id="aa092-134">Application always renders as if it is on a display with a DPI value of 96.</span></span> |  <span data-ttu-id="aa092-135">La aplicación se estira en mapa de bits al tamaño esperado en pantallas principales y secundarias.</span><span class="sxs-lookup"><span data-stu-id="aa092-135">Application is bitmap stretched to expected size on primary and secondary displays.</span></span>    |
|<span data-ttu-id="aa092-136">Reconocimiento de PPP de sistema</span><span class="sxs-lookup"><span data-stu-id="aa092-136">System DPI aware</span></span> |  <span data-ttu-id="aa092-137">La aplicación detecta el valor de PPP del monitor principal conectado al inicio de sesión de Windows, pero no responde a cambios de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-137">Application detects the DPI of the primary connected monitor at Windows login but cannot respond to DPI changes.</span></span> <span data-ttu-id="aa092-138">Para obtener más información, vea la sección [configurar Windows para corregir aplicaciones borrosas](#configure-windows-to-fix-blurry-apps) de este artículo.</span><span class="sxs-lookup"><span data-stu-id="aa092-138">For more information, see the [Configure Windows to fix blurry apps](#configure-windows-to-fix-blurry-apps) section in this article.</span></span>  | <span data-ttu-id="aa092-139">La aplicación se estira en mapa de bits cuando se mueve a una nueva pantalla con un valor de PPP diferente.</span><span class="sxs-lookup"><span data-stu-id="aa092-139">Application is bitmap stretched when moved to a new display with a different DPI.</span></span>    |
|<span data-ttu-id="aa092-140">Reconocimiento de PPP por monitor</span><span class="sxs-lookup"><span data-stu-id="aa092-140">Per Monitor DPI aware</span></span> |  <span data-ttu-id="aa092-141">La aplicación es capaz de volver a dibujarse correctamente cuando cambie el valor de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-141">Application is capable of redrawing itself correctly when the DPI changes.</span></span>  |   <span data-ttu-id="aa092-142">Windows le enviará notificaciones de PPP a ventanas de nivel superior de la aplicación para que pueda volver a dibujarse cuando cambie el valor de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-142">Windows will send DPI notifications to top-level windows in the application so that it can redraw when the DPI changes.</span></span>     |
|<span data-ttu-id="aa092-143">V2 por monitor</span><span class="sxs-lookup"><span data-stu-id="aa092-143">Per Monitor v2</span></span> |  <span data-ttu-id="aa092-144">La aplicación es capaz de volver a dibujarse correctamente cuando cambie el valor de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-144">Application is capable of redrawing itself correctly when the DPI changes.</span></span>  |   <span data-ttu-id="aa092-145">Windows le enviará notificaciones de PPP a ventanas de nivel superior y secundarias para que la aplicación pueda volver a dibujarse cuando cambie el valor de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-145">Windows will send DPI notifications to both top-level and child windows so that the application can redraw when the DPI changes.</span></span> |

## <a name="how-office-supports-dpi-scaling"></a><span data-ttu-id="aa092-146">Compatibilidad de Office con el ajuste de PPP</span><span class="sxs-lookup"><span data-stu-id="aa092-146">How Office supports DPI scaling</span></span>

<span data-ttu-id="aa092-147">El factor más importante para determinar cómo la solución de Office puede controlar el ajuste de PPP es ver si la solución es una ventana de nivel superior o una ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="aa092-147">The most significant factor in determining how your Office solution can handle DPI scaling is whether your solution is a top-level window, or a child window.</span></span> <span data-ttu-id="aa092-148">La siguiente imagen muestra algunos ejemplos de soluciones de Office que funcionan como ventanas de nivel superior o secundarias y el modo de reconocimiento de PPP que usarán en la actualización de abril 2018 de Windows (1803) y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="aa092-148">The following picture shows a few examples of Office solutions running as top-level or child windows, and which DPI awareness mode they will use on Windows April 2018 Update (1803) and later.</span></span>

![Excel que hospeda un control ActiveX y el panel de tareas personalizado como ventanas secundarias.](./media/office-dpi-awareness-for-solution-types.png)

<span data-ttu-id="aa092-152">En esta imagen:</span><span class="sxs-lookup"><span data-stu-id="aa092-152">In this image:</span></span>
- <span data-ttu-id="aa092-153">La ventana de nivel superior VSTO o COM cuenta con el reconocimiento de PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="aa092-153">The COM/VSTO top-level window is Per Monitor DPI aware.</span></span>
- <span data-ttu-id="aa092-154">La ventana secundaria del control ActiveX cuenta con el reconocimiento de PPP de sistema.</span><span class="sxs-lookup"><span data-stu-id="aa092-154">The ActiveX control child window is System DPI aware.</span></span>
- <span data-ttu-id="aa092-155">La ventana de nivel superior de Office cuenta con el reconocimiento de PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="aa092-155">The Office top-level window is Per Monitor DPI aware.</span></span>
- <span data-ttu-id="aa092-156">La ventana secundaria del panel de tareas personalizado cuenta con el reconocimiento de PPP de sistema.</span><span class="sxs-lookup"><span data-stu-id="aa092-156">The custom task pane child window is System DPI aware.</span></span>

## <a name="managing-thread-dpi-context"></a><span data-ttu-id="aa092-157">Administrar el contexto de PPP de subprocesos</span><span class="sxs-lookup"><span data-stu-id="aa092-157">Managing thread DPI context</span></span>

<span data-ttu-id="aa092-158">Cuando se inicie la aplicación host de Office, su subproceso principal se ejecuta en el contexto de reconocimiento de PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="aa092-158">When the host Office app starts, its main thread runs in Per Monitor DPI aware context.</span></span> <span data-ttu-id="aa092-159">Cuando el código de solución crea subprocesos o recibe llamadas de Office, debe administrar el contexto de PPP de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="aa092-159">When your solution code creates threads, or receives calls from Office, you need to manage the thread DPI context.</span></span>

### <a name="creating-new-threads-with-the-correct-dpi-context"></a><span data-ttu-id="aa092-160">Crear nuevos subprocesos con el contexto de PPP correcto</span><span class="sxs-lookup"><span data-stu-id="aa092-160">Creating new threads with the correct DPI context</span></span>

<span data-ttu-id="aa092-161">Si su solución crea subprocesos adicionales, Office los obligará al contexto de reconocimiento de PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="aa092-161">If your solution creates additional threads, Office will force the threads into Per Monitor DPI aware context.</span></span> <span data-ttu-id="aa092-162">Si el código se espera un contexto diferente, debe usar la función [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) para establecer el reconocimiento de PPP de subproceso esperado.</span><span class="sxs-lookup"><span data-stu-id="aa092-162">If your code expects a different context, you need to use the [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) function to set the expected thread DPI awareness.</span></span> 

### <a name="build-a-context-block-for-incoming-thread-calls"></a><span data-ttu-id="aa092-163">Crear un bloque de contexto para las llamadas entrantes de subprocesos</span><span class="sxs-lookup"><span data-stu-id="aa092-163">Build a context block for incoming thread calls</span></span>

![Diagrama que muestra el bloque de contexto en la aplicación de Office que cambia el subproceso al contexto de reconocimiento de sistema en llamadas a la ventana de nivel superior.](./media/thread-dpi-awareness-context-block.png)

<span data-ttu-id="aa092-165">La solución interactúa con su aplicación host de Office, por lo que recibirá llamadas entrantes para su solución de Office como devoluciones de llamadas de eventos.</span><span class="sxs-lookup"><span data-stu-id="aa092-165">Your solution will interact with its host Office app, so you will have incoming calls to your solution from Office such as event callbacks.</span></span> <span data-ttu-id="aa092-166">Cuando Office llama la solución, cuenta con un bloque de contexto que fuerza el contexto de subprocesos en el contexto de reconocimiento de PPP de sistema.</span><span class="sxs-lookup"><span data-stu-id="aa092-166">When Office calls your solution, it has a context block that forces the thread context to be in System DPI Aware context.</span></span> <span data-ttu-id="aa092-167">Debe cambiar el contexto de subprocesos para que coincida con el reconocimiento de PPP de la ventana.</span><span class="sxs-lookup"><span data-stu-id="aa092-167">You must change the thread context to match the DPI awareness of your window.</span></span> <span data-ttu-id="aa092-168">Puede implementar un bloque de contexto similar para cambiar el contexto de subprocesos en llamadas entrantes.</span><span class="sxs-lookup"><span data-stu-id="aa092-168">You can implement a similar context block to switch the thread context on incoming calls.</span></span> <span data-ttu-id="aa092-169">Use la función [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) para cambiar el contexto para que coincida con el contexto de la ventana.</span><span class="sxs-lookup"><span data-stu-id="aa092-169">Use the [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) function to change the context to match your window context.</span></span> 

> [!NOTE]
> <span data-ttu-id="aa092-170">El bloque de contexto debe restaurar el contexto de subprocesos de PPP original antes de llamar a los demás componentes fuera de su código de la solución.</span><span class="sxs-lookup"><span data-stu-id="aa092-170">Your context block should restore the original DPI thread context before calling other components outside of your solution code.</span></span>

#### <a name="managed-code-context-block"></a><span data-ttu-id="aa092-171">Bloque de contexto de código administrado</span><span class="sxs-lookup"><span data-stu-id="aa092-171">Managed code context block</span></span>

<span data-ttu-id="aa092-172">El ejemplo de código siguiente muestra cómo crear su propio bloque de contexto.</span><span class="sxs-lookup"><span data-stu-id="aa092-172">The following example code shows how to construct your own context block.</span></span>

```csharp
public struct DPI_AWARENESS_CONTEXT
        {
            private IntPtr value;

            private DPI_AWARENESS_CONTEXT(IntPtr value)
            {
                this.value = value;
            }

            public static implicit operator DPI_AWARENESS_CONTEXT(IntPtr value)
            {
                return new DPI_AWARENESS_CONTEXT(value);
            }

            public static implicit operator IntPtr(DPI_AWARENESS_CONTEXT context)
            {
                return context.value;
            }

            public static bool operator ==(IntPtr context1, DPI_AWARENESS_CONTEXT context2)
            {
                return AreDpiAwarenessContextsEqual(context1, context2);
            }

            public static bool operator !=(IntPtr context1, DPI_AWARENESS_CONTEXT context2)
            {
                return !AreDpiAwarenessContextsEqual(context1, context2);
            }

            public override bool Equals(object obj)
            {
                return base.Equals(obj);
            }

            public override int GetHashCode()
            {
                return base.GetHashCode();
            }
        }

        private static DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_HANDLE = IntPtr.Zero;

        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_INVALID = IntPtr.Zero;
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_UNAWARE = new IntPtr(-1);
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_SYSTEM_AWARE = new IntPtr(-2);
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE = new IntPtr(-3);
        public static readonly DPI_AWARENESS_CONTEXT DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2 = new IntPtr(-4);

        public static DPI_AWARENESS_CONTEXT[] DpiAwarenessContexts =
        {
            DPI_AWARENESS_CONTEXT_UNAWARE,
            DPI_AWARENESS_CONTEXT_SYSTEM_AWARE,
            DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE,
            DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2
        };

class DPIContextBlock : IDisposable
    {
        private DPI_AWARENESS_CONTEXT resetContext;
        private bool disposed = false;

        public DPIContextBlock(DPI_AWARENESS_CONTEXT contextSwitchTo)
        {
            resetContext = SetThreadDpiAwarenessContext(contextSwitchTo);
         }

        public void Dispose()
        {
            Dispose(true);
            GC.SuppressFinalize(this);
        }

        protected virtual void Dispose(bool disposing)
        {
            if (!disposed)
            {
                if (disposing)
                {
                    SetThreadDpiAwarenessContext(resetContext);
                }
            }
            disposed = true;
        }
    }
```

#### <a name="native-code-context-block"></a><span data-ttu-id="aa092-173">Bloque de contexto de código nativo</span><span class="sxs-lookup"><span data-stu-id="aa092-173">Native code context block</span></span>

```cpp
#include <winuser.h>
/* DpiAwarenessContextBlock can be used to simplify setting and resetting the DPI_AWARENESS_CONTEXT of
the current thread.  When the object is constructed, the DPI_AWARENESS_CONTEXT is set, and when the object is
destructed, the DPI awareness context is reverted to the previous awareness context at construct time.

This object allows us to write code such as:

// Thread state is currently DPI_AWARENESS_SYSTEM_AWARE
if (condition)
{
DpiAwarenessContextBlock perMonitorAware(DPI_AWARENESS_PER_MONITOR_AWARE);
... // Create a top-level hwnd with the current thread state, DPI_AWARENESS_PER_MONITOR_AWARE
}
// Thread state automatically returns to DPI_AWARENESS_SYSTEM_AWARE

*/
class DpiAwarenessContextBlock
{
public:
      DpiAwarenessContextBlock(DPI_AWARENESS_CONTEXT dpiContext) noexcept;
      ~DpiAwarenessContextBlock();

      // Copy and move are not to be used with these context objects
      DpiAwarenessContextBlock(const DpiAwarenessContextBlock&) = delete;
      DpiAwarenessContextBlock(DpiAwarenessContextBlock&&) = delete;

private:
      DPI_AWARENESS_CONTEXT m_contextReversalType;
      bool m_doContextSwitch;
};

inline DpiAwarenessContextBlock::DpiAwarenessContextBlock(DPI_AWARENESS_CONTEXT dpiContext) noexcept
{
      m_contextReversalType = SetThreadDpiAwarenessContext(dpiContext);
}

inline DpiAwarenessContextBlock::~DpiAwarenessContextBlock()
{
      SetThreadDpiAwarenessContext(m_contextReversalType);
}
```

<h2 id="top-level-window-management"><span data-ttu-id="aa092-174">Administración de ventanas de nivel superior</span><span class="sxs-lookup"><span data-stu-id="aa092-174">Top-level window management</span></span></h2>

<span data-ttu-id="aa092-175">Al iniciar aplicaciones de Office, se realiza una llamada a [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) como DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE.</span><span class="sxs-lookup"><span data-stu-id="aa092-175">When Office applications start, a call is made to [SetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-setthreaddpiawarenesscontext) as DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE.</span></span> <span data-ttu-id="aa092-176">En este contexto, los cambios de PPP se envían a HWND de cualquier ventana de nivel superior en el proceso que se está ejecutando según el reconocimiento de PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="aa092-176">In this context, DPI changes are sent to the HWND of any top-level windows in the process that are running as Per Monitor DPI aware.</span></span> <span data-ttu-id="aa092-177">Las ventanas de nivel superior son la ventana de la aplicación de Office y cualquier ventana de nivel superior adicional creada por la solución.</span><span class="sxs-lookup"><span data-stu-id="aa092-177">Top-level windows are the Office application window, and any additional top-level windows created by your solution.</span></span> <span data-ttu-id="aa092-178">Cuando una aplicación de Office se mueve a una nueva pantalla, recibe una notificación para que pueda escalar dinámicamente y dibujarse correctamente con el valor PPP de la nueva pantalla.</span><span class="sxs-lookup"><span data-stu-id="aa092-178">When an Office application is moved to a new display, it gets notified so that it can dynamically scale and draw correctly in the DPI of the new display.</span></span> <span data-ttu-id="aa092-179">La solución de Office puede crear ventanas de nivel superior en cualquier modo de reconocimiento de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-179">Your Office solution can create top-level windows that are in any DPI awareness mode.</span></span> <span data-ttu-id="aa092-180">Las ventanas de nivel superior también pueden responder a los cambios de PPP al escuchar mensajes de Windows para los cambios.</span><span class="sxs-lookup"><span data-stu-id="aa092-180">Your top-level windows can also respond to DPI changes by listening to Windows messages for the changes.</span></span>

<span data-ttu-id="aa092-181">Si crea ventanas secundarias que están relacionadas a la ventana de nivel superior, también puede establecerlas con cualquier modo de reconocimiento de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-181">If you create child windows that are parented to your top-level window, you can also set them to any DPI awareness mode.</span></span> <span data-ttu-id="aa092-182">Sin embargo, si usa el modo de reconocimiento de PPP por monitor, las ventanas secundarias no recibirán notificaciones de cambio de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-182">However, if you use Per Monitor DPI aware mode, your child windows will not receive DPI change notifications.</span></span>  <span data-ttu-id="aa092-183">Para obtener más información sobre los modos de reconocimiento de PPP de Windows, vea [Desarrollo de aplicaciones de escritorio con valores altos de PPP en Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).</span><span class="sxs-lookup"><span data-stu-id="aa092-183">For more information about Windows DPI awareness modes, see [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows).</span></span>

## <a name="child-window-management"></a><span data-ttu-id="aa092-184">Administración de ventanas secundarias</span><span class="sxs-lookup"><span data-stu-id="aa092-184">Child window management</span></span>

<span data-ttu-id="aa092-185">Al trabajar con controles ActiveX y paneles de tareas personalizados, Office creará la ventana secundaria para su solución.</span><span class="sxs-lookup"><span data-stu-id="aa092-185">When working with ActiveX controls and custom task panes, Office creates the child window for your solution.</span></span> <span data-ttu-id="aa092-186">Puede crear ventanas secundarias adicionales, pero debe ser conscientes del reconocimiento de PPP de la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="aa092-186">You can create additional child windows, but you have to be aware of the parent window DPI awareness.</span></span> <span data-ttu-id="aa092-187">Office se ejecuta en modo de reconocimiento de PPP por monitor, lo que significa que ninguna ventana secundaria en su solución recibirá notificaciones de cambio de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-187">Office runs in Per Monitor DPI awareness mode, which means any child windows in your solution will not get DPI change notifications.</span></span> <span data-ttu-id="aa092-188">Solo el modo v2 por monitor admite el envío de cambios de PPP a ventanas secundarias (Office no es compatible con v2 por monitor).</span><span class="sxs-lookup"><span data-stu-id="aa092-188">Only Per Monitor v2 mode supports sending DPI changes to child windows (Office does not support Per Monitor v2).</span></span> <span data-ttu-id="aa092-189">Sin embargo, hay una solución alternativa para los controles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="aa092-189">However, for ActiveX controls, there is a workaround.</span></span> <span data-ttu-id="aa092-190">Para obtener más información, vea la sección [Controles ActiveX](#activex-controls) más adelante en este artículo.</span><span class="sxs-lookup"><span data-stu-id="aa092-190">For more information, see the [ActiveX controls](#activex-controls) section later in this article.</span></span>

> [!NOTE]
> <span data-ttu-id="aa092-191">Si la ventana secundaria crea una ventana de nivel superior, puede usar cualquier modo de reconocimiento de PPP para la nueva ventana de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="aa092-191">If your child window creates a top-level window, you can use any DPI awareness mode for the new top-level window.</span></span> <span data-ttu-id="aa092-192">Para obtener más información sobre cómo administrar ventanas de nivel superior, consulte la sección [Administración de la ventana de nivel superior](#top-level-window-management) de este artículo.</span><span class="sxs-lookup"><span data-stu-id="aa092-192">For more information about managing top-level windows, see the [Top-level window management](#top-level-window-management) section in this article.</span></span>

<span data-ttu-id="aa092-193">Verá dos modos PPP diferentes aplicados a la ventana secundaria, según la versión de Windows 10 en la que se ejecuta Office.</span><span class="sxs-lookup"><span data-stu-id="aa092-193">You will see two different DPI modes applied to your child window, depending on which version of Windows 10 Office is running on.</span></span>

### <a name="office-dpi-behavior-on-windows-fall-creators-update-1709"></a><span data-ttu-id="aa092-194">Comportamiento de PPP de Office en Windows Fall Creators Update (1709)</span><span class="sxs-lookup"><span data-stu-id="aa092-194">Office DPI behavior on Windows Fall Creators Update (1709)</span></span>

<span data-ttu-id="aa092-195">Como las aplicaciones de Office usan el modo de reconocimiento por monitor, las ventanas secundarias de su solución también se crearán en modo de reconocimiento de PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="aa092-195">Because Office apps use Per Monitor awareness mode, your solution’s child windows will also be created in Per Monitor DPI awareness mode.</span></span> <span data-ttu-id="aa092-196">Esto significa que Windows espera que su solución se actualice al dibujar con un nuevo valor de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-196">This means Windows expects your solution to update when drawing in a new DPI.</span></span>  <span data-ttu-id="aa092-197">Como la ventana no puede recibir notificaciones de cambio de PPP, la interfaz de usuario de la solución podría ser incorrecta.</span><span class="sxs-lookup"><span data-stu-id="aa092-197">Because your window cannot get DPI change notifications, your solution’s UI might be incorrect.</span></span> 

![Diagrama que muestra ventanas secundarias que se ejecutan en el contexto de reconocimiento de PPP por monitor en Windows Fall Creators Update (1709).](./media/office-dpi-behavior-on-windows-fall-creators-update.png)

### <a name="office-dpi-behavior-on-windows-april-2018-update-1803"></a><span data-ttu-id="aa092-199">Comportamiento de PPP de Office en la actualización de abril de 2018 de Windows (1803)</span><span class="sxs-lookup"><span data-stu-id="aa092-199">Office DPI behavior on Windows April 2018 Update (1803)</span></span>

<span data-ttu-id="aa092-200">Con la actualización de abril de 2018 de Windows (1803) y versiones posteriores, el comportamiento de hospedaje de PPP de Office usa el ajuste de PPP de modo mixto para algunos escenarios.</span><span class="sxs-lookup"><span data-stu-id="aa092-200">With Windows April 2018 (1803) update and later, The Office DPI hosting behavior uses mixed-mode DPI scaling for some scenarios.</span></span> <span data-ttu-id="aa092-201">Esto permite a las ventanas con reconocimiento de PPP de sistema que estén relacionadas con las ventanas de Office establecidas con el reconocimiento de PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="aa092-201">This allows System DPI Aware windows to be parented to Office windows set to Per Monitor DPI aware.</span></span> <span data-ttu-id="aa092-202">Esto ayuda a garantizar la compatibilidad mejorada al cambiar el valor de PPP cuando las ventanas son estiradas en mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="aa092-202">This helps to ensure improved compatibility when the DPI changes when the windows are bitmap stretched.</span></span> <span data-ttu-id="aa092-203">Las ventanas todavía podrían parecer borrosas por el estiramiento en mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="aa092-203">The windows might still be blurry from the bitmap stretching.</span></span>

![Diagrama que muestra ventanas secundarias que se ejecutan en el contexto de reconocimiento de PPP de sistema en la actualización de abril de 2018 de Windows (1803).](./media/office-dpi-behavior-on-windows-april-2018-update.png)

<span data-ttu-id="aa092-205">Al crear nuevas ventanas secundarias, asegúrese de que coincidan con el reconocimiento de PPP de la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="aa092-205">When you create new child windows, be sure they match the DPI awareness of their parent window.</span></span> <span data-ttu-id="aa092-206">Puede usar la función [GetWindowdpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) para obtener el reconocimiento de PPP de la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="aa092-206">You can use the [GetWindowdpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) function to get the DPI awareness of the parent window.</span></span> <span data-ttu-id="aa092-207">Para más información sobre la coherencia de reconocimiento de PPP, consulte la sección "Reinicio forzado del reconocimiento de todo el proceso de PPP" en [Desarrollo de aplicaciones de escritorio con un valor alto de PPP en Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).</span><span class="sxs-lookup"><span data-stu-id="aa092-207">For more information about DPI awareness consistency, see the “Forced reset of process-wide DPI awareness” section in [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).</span></span>

> [!NOTE]
> <span data-ttu-id="aa092-208">No puede confiar en el reconocimiento de PPP de proceso porque puede devolver [PROCESS_SYSTEM_DPI_AWARE](https://docs.microsoft.com/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness) incluso cuando el contexto de reconocimiento de PPP de subprocesos principal de la aplicación es [DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE](https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context).</span><span class="sxs-lookup"><span data-stu-id="aa092-208">You can’t rely on the Process DPI Awareness as it might return [PROCESS_SYSTEM_DPI_AWARE](https://docs.microsoft.com/windows/desktop/api/shellscalingapi/ne-shellscalingapi-process_dpi_awareness) even when the application main thread DPI awareness context is [DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE](https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context).</span></span> <span data-ttu-id="aa092-209">Use la función [GetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext) para obtener el contexto de reconocimiento de PPP de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="aa092-209">Use the [GetThreadDpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getthreaddpiawarenesscontext) function to get the thread DPI awareness context.</span></span>

## <a name="office-and-windows-dpi-compatibility-settings"></a><span data-ttu-id="aa092-210">Configuración de compatibilidad de PPP de Windows y Office</span><span class="sxs-lookup"><span data-stu-id="aa092-210">Office and Windows DPI compatibility settings</span></span>

<span data-ttu-id="aa092-211">Cuando los usuarios encuentran complementos o soluciones que no se representan correctamente, algunas opciones de compatibilidad sirven para corregir el problema.</span><span class="sxs-lookup"><span data-stu-id="aa092-211">When users encounter add-ins or solutions that are not rendering correctly, some compatibility settings can help correct the problem.</span></span>

<h3 id="office-compatibility"><span data-ttu-id="aa092-212">Configurar Office para optimizar la compatibilidad</span><span class="sxs-lookup"><span data-stu-id="aa092-212">Configure Office to optimize for compatibility</span></span></h3>

<span data-ttu-id="aa092-213">Office dispone de una configuración para optimizar la compatibilidad al pasar a escalas de PPP diferentes en pantallas diferentes.</span><span class="sxs-lookup"><span data-stu-id="aa092-213">Office has a setting to optimize for compatibility when moving to different DPI scales on different screens.</span></span> <span data-ttu-id="aa092-214">El modo de compatibilidad deshabilita el ajuste de PPP para que todo en Office sea estirado en mapa de bits cuando se mueve a una pantalla con un ajuste de PPP diferente.</span><span class="sxs-lookup"><span data-stu-id="aa092-214">The compatibility mode disables DPI scaling so that everything in Office is bitmap stretched when moved to a display using different DPI scaling.</span></span> 

<span data-ttu-id="aa092-215">El modo de compatibilidad obliga a Office a ejecutarse en modo de reconocimiento de PPP de sistema.</span><span class="sxs-lookup"><span data-stu-id="aa092-215">The compatibility mode forces Office to run in System DPI aware mode.</span></span> <span data-ttu-id="aa092-216">Esto hace que las ventanas de aplicaciones se estiren en mapa de bits y puede tener el efecto secundario de una apariencia borrosa.</span><span class="sxs-lookup"><span data-stu-id="aa092-216">This causes application windows to bitmap stretch and can have a side effect of a blurry appearance.</span></span> <span data-ttu-id="aa092-217">La solución de Office no puede controlar esta configuración porque la selecciona el usuario.</span><span class="sxs-lookup"><span data-stu-id="aa092-217">Your Office solution cannot control this setting because the user chooses it.</span></span> <span data-ttu-id="aa092-218">Usar el modo de compatibilidad de pantalla soluciona la mayoría de problemas de dibujo.</span><span class="sxs-lookup"><span data-stu-id="aa092-218">Using the display compatibility mode solves most drawing problems.</span></span> <span data-ttu-id="aa092-219">Para obtener más información, vea [Soporte técnico de Office para pantallas de alta definición](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span><span class="sxs-lookup"><span data-stu-id="aa092-219">For more information, see [Office support for high definition displays](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span></span> 

### <a name="configure-windows-to-fix-blurry-apps"></a><span data-ttu-id="aa092-220">Configurar Windows para corregir aplicaciones borrosas</span><span class="sxs-lookup"><span data-stu-id="aa092-220">Configure Windows to fix blurry apps</span></span>

<span data-ttu-id="aa092-221">Windows 10 (versión 1803) y versiones posteriores disponen de una configuración para corregir aplicaciones para que no sean borrosas.</span><span class="sxs-lookup"><span data-stu-id="aa092-221">Windows 10 (Version 1803) and later has a setting to fix apps so they’re not blurry.</span></span> <span data-ttu-id="aa092-222">Esta es otra configuración para probar si no se está representando correctamente la solución.</span><span class="sxs-lookup"><span data-stu-id="aa092-222">This is another setting to try if your solution is not rendering correctly.</span></span> <span data-ttu-id="aa092-223">La solución de Office no puede controlar esta configuración porque la selecciona el usuario.</span><span class="sxs-lookup"><span data-stu-id="aa092-223">Your Office solution cannot control this setting because the user chooses it.</span></span> <span data-ttu-id="aa092-224">Para obtener más información, vea [Corregir aplicaciones que se vean borrosas en Windows 10](https://support.microsoft.com/en-us/help/4091364/windows-10-fix-blurry-apps).</span><span class="sxs-lookup"><span data-stu-id="aa092-224">For more information, see [Fix apps that appear blurry in Windows 10](https://support.microsoft.com/en-us/help/4091364/windows-10-fix-blurry-apps).</span></span>

## <a name="how-to-support-dpi-scaling-in-your-solution"></a><span data-ttu-id="aa092-225">Compatibilidad del ajuste de PPP en su solución</span><span class="sxs-lookup"><span data-stu-id="aa092-225">How to support DPI scaling in your solution</span></span>

<span data-ttu-id="aa092-226">Algunas soluciones pueden recibir y responder a los cambios de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-226">Some solutions can receive and respond to DPI changes.</span></span> <span data-ttu-id="aa092-227">Algunas tienen una solución alternativa si no pueden recibir notificaciones.</span><span class="sxs-lookup"><span data-stu-id="aa092-227">Some have a workaround if they cannot receive notifications.</span></span> <span data-ttu-id="aa092-228">En la siguiente tabla se enumeran los detalles de cada tipo de solución.</span><span class="sxs-lookup"><span data-stu-id="aa092-228">The following table lists the details for each solution type.</span></span>

<table>
    <thead>
        <tr>
            <th><span data-ttu-id="aa092-229">Tipo de solución</span><span class="sxs-lookup"><span data-stu-id="aa092-229">Solution Type</span></span></th>
            <th><span data-ttu-id="aa092-230">Tipo de ventana</span><span class="sxs-lookup"><span data-stu-id="aa092-230">Window type</span></span></th>
            <th><span data-ttu-id="aa092-231">Puede responder al ajuste de PPP</span><span class="sxs-lookup"><span data-stu-id="aa092-231">Can respond to DPI scaling</span></span></th>
            <th><span data-ttu-id="aa092-232">Más detalles</span><span class="sxs-lookup"><span data-stu-id="aa092-232">More details</span></span></th>
        </tr>
    </thead>
<tbody>
    <tr>
        <td rowspan="2"><span data-ttu-id="aa092-233"><a href="#vsto-add-ins">Complementos VSTO</a></span><span class="sxs-lookup"><span data-stu-id="aa092-233"><a href="#vsto-add-ins">VSTO Add-in</a></span></span></td>
        <td><span data-ttu-id="aa092-234">Parte superior y sus descendientes</span><span class="sxs-lookup"><span data-stu-id="aa092-234">Top and its descendants</span></span></td>
        <td><span data-ttu-id="aa092-235">Sí</span><span class="sxs-lookup"><span data-stu-id="aa092-235">Yes</span></span></td>
        <td><span data-ttu-id="aa092-236">Vea <a href="#vsto-add-ins">Guía para el complemento VSTO</a>.</span><span class="sxs-lookup"><span data-stu-id="aa092-236">See <a href="#vsto-add-ins">VSTO add-in guidance</a>.</span></span></td>
    </tr>
<tr>
        <td><span data-ttu-id="aa092-237">Elementos secundarios relacionados con la ventana de Office</span><span class="sxs-lookup"><span data-stu-id="aa092-237">Child parented to Office window</span></span></td>
        <td><span data-ttu-id="aa092-238">No</span><span class="sxs-lookup"><span data-stu-id="aa092-238">No</span></span></td>
        <td><span data-ttu-id="aa092-239">Vea <a href="#office-compatibility">Configurar Office para optimizar la compatibilidad</a>.</span><span class="sxs-lookup"><span data-stu-id="aa092-239">See <a href="#office-compatibility">Configure Office to optimize for compatibility</a>.</span></span></td>
</tr>
    <tr>
        <td rowspan="2"><span data-ttu-id="aa092-240"><a href="#custom-task-panes">Panel de tareas personalizado</a></span><span class="sxs-lookup"><span data-stu-id="aa092-240"><a href="#custom-task-panes">Custom task pane</a></span></span></td>
        <td><span data-ttu-id="aa092-241">Parte superior y sus descendientes</span><span class="sxs-lookup"><span data-stu-id="aa092-241">Top and its descendants</span></span></td>
        <td><span data-ttu-id="aa092-242">Sí</span><span class="sxs-lookup"><span data-stu-id="aa092-242">Yes</span></span></td>
        <td><span data-ttu-id="aa092-243">Vea la <a href="#top-level-window-management">Guía de la ventana de nivel superior</a>.</span><span class="sxs-lookup"><span data-stu-id="aa092-243">See <a href="#top-level-window-management">top-level window guidance</a>.</span></span></td>
    </tr>
<tr>
        <td><span data-ttu-id="aa092-244">Elementos secundarios relacionados con la ventana de Office</span><span class="sxs-lookup"><span data-stu-id="aa092-244">Child parented to Office window</span></span></td>
        <td><span data-ttu-id="aa092-245">No</span><span class="sxs-lookup"><span data-stu-id="aa092-245">No</span></span></td>
        <td><span data-ttu-id="aa092-246">Vea <a href="#office-compatibility">Configurar Office para optimizar la compatibilidad</a>.</span><span class="sxs-lookup"><span data-stu-id="aa092-246">See <a href="#office-compatibility">Configure Office to optimize for compatibility</a>.</span></span></td>
</tr>
    <tr>
        <td rowspan="2"><span data-ttu-id="aa092-247"><a href="#com-add-ins">Complemento COM</a></span><span class="sxs-lookup"><span data-stu-id="aa092-247"><a href="#com-add-ins">COM Add-in</a></span></span></td>
        <td><span data-ttu-id="aa092-248">Parte superior y sus descendientes</span><span class="sxs-lookup"><span data-stu-id="aa092-248">Top and its descendants</span></span></td>
        <td><span data-ttu-id="aa092-249">Sí</span><span class="sxs-lookup"><span data-stu-id="aa092-249">Yes</span></span></td>
        <td><span data-ttu-id="aa092-250">Vea <a href="#com-add-ins">Guía para el complemento COM</a>.</span><span class="sxs-lookup"><span data-stu-id="aa092-250">See <a href="#com-add-ins">COM Add-in guidance</a>.</span></span></td>
    </tr>
<tr>
        <td><span data-ttu-id="aa092-251">Elementos secundarios relacionados con la ventana de Office</span><span class="sxs-lookup"><span data-stu-id="aa092-251">Child parented to Office window</span></span></td>
        <td><span data-ttu-id="aa092-252">No</span><span class="sxs-lookup"><span data-stu-id="aa092-252">No</span></span></td>
        <td><span data-ttu-id="aa092-253">Vea <a href="#office-compatibility">Configurar Office para optimizar la compatibilidad</a>.</span><span class="sxs-lookup"><span data-stu-id="aa092-253">See <a href="#office-compatibility">Configure Office to optimize for compatibility</a>.</span></span></td>
</tr>
    <tr>
        <td rowspan="2"><span data-ttu-id="aa092-254"><a href="#activex-controls">Control ActiveX</a></span><span class="sxs-lookup"><span data-stu-id="aa092-254"><a href="#activex-controls">ActiveX control</a></span></span></td>
        <td><span data-ttu-id="aa092-255">Parte superior y sus descendientes</span><span class="sxs-lookup"><span data-stu-id="aa092-255">Top and its descendants</span></span></td>
        <td><span data-ttu-id="aa092-256">Sí</span><span class="sxs-lookup"><span data-stu-id="aa092-256">Yes</span></span></td>
        <td><span data-ttu-id="aa092-257">Vea <a href="#activex-controls">Guía de control ActiveX</a>.</span><span class="sxs-lookup"><span data-stu-id="aa092-257">See <a href="#activex-controls">ActiveX control guidance</a>.</span></span></td>
    </tr>
    <tr>
        <td><span data-ttu-id="aa092-258">Elementos secundarios relacionados con la ventana de Office</span><span class="sxs-lookup"><span data-stu-id="aa092-258">Child parented to Office window</span></span></td>
        <td><span data-ttu-id="aa092-259">Sí</span><span class="sxs-lookup"><span data-stu-id="aa092-259">Yes</span></span></td>
    </tr>
    <tr>
        <td><span data-ttu-id="aa092-260"><a href="#web-add-ins">Complemento web</a></span><span class="sxs-lookup"><span data-stu-id="aa092-260"><a href="#web-add-ins">Web Add-in</a></span></span></td>
        <td><span data-ttu-id="aa092-261">ND</span><span class="sxs-lookup"><span data-stu-id="aa092-261">NA</span></span></td>
        <td><span data-ttu-id="aa092-262">Sí</span><span class="sxs-lookup"><span data-stu-id="aa092-262">Yes</span></span></td>
        <td><span data-ttu-id="aa092-263">Vea <a href="#web-add-ins">Guía de complemento web de Office</a>.</span><span class="sxs-lookup"><span data-stu-id="aa092-263">See <a href="#web-add-ins">Office web add-in guidance</a>.</span></span></td>
    </tr>
    <tr>
        <td><span data-ttu-id="aa092-264"><a href="#ribbon-extensibility">Extensión de la cinta de opciones</a></span><span class="sxs-lookup"><span data-stu-id="aa092-264"><a href="#ribbon-extensibility">Ribbon extension</a></span></span></td>
        <td><span data-ttu-id="aa092-265">NA</span><span class="sxs-lookup"><span data-stu-id="aa092-265">NA</span></span></td>
        <td><span data-ttu-id="aa092-266">NA</span><span class="sxs-lookup"><span data-stu-id="aa092-266">NA</span></span></td>
        <td><span data-ttu-id="aa092-267">Vea <a href="#ribbon-extensibility">Guía de extensión de la cinta de opciones</a>.</span><span class="sxs-lookup"><span data-stu-id="aa092-267">See <a href="#ribbon-extensibility">Ribbon extension guidance</a>.</span></span></td>
    </tr>
    <tr>
        <td><span data-ttu-id="aa092-268"><a href="#ole">Cliente o servidor OLE</a></span><span class="sxs-lookup"><span data-stu-id="aa092-268"><a href="#ole">OLE server or client</a></span></span></td>
        <td><span data-ttu-id="aa092-269">NA</span><span class="sxs-lookup"><span data-stu-id="aa092-269">NA</span></span></td>
        <td><span data-ttu-id="aa092-270">NA</span><span class="sxs-lookup"><span data-stu-id="aa092-270">NA</span></span></td>
        <td><span data-ttu-id="aa092-271">Vea <a href="#ole">Guía de cliente y servidor OLE</a>.</span><span class="sxs-lookup"><span data-stu-id="aa092-271">See <a href="#ole">OLE server/client guidance</a>.</span></span></td>
    </tr>
</tbody>
</table>

<h3 id="vsto-add-ins"><span data-ttu-id="aa092-272">Complemento VSTO</span><span class="sxs-lookup"><span data-stu-id="aa092-272">VSTO add-in</span></span></h3>

<span data-ttu-id="aa092-273">Si el complemento VSTO crea ventanas secundarias que están relacionadas con cualquier ventana de Office, asegúrese de que coincidan con el reconocimiento de PPP de la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="aa092-273">If your VSTO add-in creates child windows that are parented to any Office windows, be sure they match the DPI awareness of their parent window.</span></span> <span data-ttu-id="aa092-274">Puede usar la función [GetWindowdpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) para obtener el reconocimiento de PPP de la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="aa092-274">You can use the [GetWindowdpiAwarenessContext](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getwindowdpiawarenesscontext) function to get the DPI awareness of the parent window.</span></span> <span data-ttu-id="aa092-275">Las ventanas secundarias no recibirán ninguna notificación de cambio de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-275">Your child windows will not get any DPI change notifications.</span></span> <span data-ttu-id="aa092-276">Si no se está representando correctamente la solución, los usuarios deberán poner Office en modo de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="aa092-276">If your solution is not rendering correctly, users will need to put Office into compatibility mode.</span></span>

<span data-ttu-id="aa092-277">Para todas las ventanas de nivel superior que crea el complemento VSTO, puede establecerlas en cualquier modo de reconocimiento de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-277">For any top-level windows your VSTO add-in creates, you can set them to any DPI awareness mode.</span></span> <span data-ttu-id="aa092-278">El ejemplo de código siguiente muestra cómo configurar el reconocimiento de PPP deseado y cómo responder a los cambios de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-278">The following sample code shows how to set up the desired DPI awareness, and how to respond to DPI changes.</span></span> <span data-ttu-id="aa092-279">También necesitará ajustar el app.config, como se describe en el artículo [Soporte de valores altos de PPP en Windows Forms](https://docs.microsoft.com/dotnet/framework/winforms/high-dpi-support-in-windows-forms).</span><span class="sxs-lookup"><span data-stu-id="aa092-279">You will also need to adjust your app.config, as described in the [High DPI support in Windows Forms](https://docs.microsoft.com/dotnet/framework/winforms/high-dpi-support-in-windows-forms) article.</span></span> 

```csharp
using System;
using System.Diagnostics;
using System.Drawing;
using System.Runtime.InteropServices;
using System.Windows.Forms;

namespace SharedModule
{
    // DpiAwareWindowsForm
    // For any top level winform you create, derive from the DpiWindowsForm class
    // if you are creating Windows Forms with the Dpi Awareness Context set to 
    // DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE or DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2
    //
    // For example, if you Window form class is defined as:
    //    public partial class TopLevelWinForm : Form
    //
    // update to:
    //    public partial class TopLevelWinForm : DpiAwareWindowsForm
    //
    // When showing the form, call SetThreadDpiAwarenessContext() or use a context block to
    // to set the desired Dpi Awareness Context.
    //
    // For example, here is code to show a Windows Form using a context block as Per Monitor Aware v2.
    //
    //    DPIContextBlock context = new DPIContextBlock(DPI_AWARENESS_CONTEXT_PER_MONITOR_AWARE_V2);
    //    TopLevelWinForm frm = new TopLevelWinForm();
    //    frm.Show();
    //
    public partial class DpiAwareWindowsForm : Form
    {
        private SizeF m_newDpi = SizeF.Empty;
        private SizeF m_oldDpi = SizeF.Empty;

        public DpiAwareWindowsForm()
        {
            this.HandleCreated += new EventHandler((sender, args) =>
            {
                m_oldDpi = m_newDpi = DPIHelper.GetDpiForWindowSizeF(this.Handle);
            });
        }

        public void OnDpiChangedEvent(RECT newRect)
        {
            this.SuspendLayout();

            // Resize form
            this.Width = newRect.Width;
            this.Height = newRect.Height;

            // Resize controls and set font sizes
            ScaleAllChildControls(this.Controls, m_oldDpi.Width, m_newDpi.Width);
            this.ResumeLayout(true);
        }

        // Additional changes may be needed for controls that set Anchor or Dock properties 
        private void ScaleAllChildControls(Control.ControlCollection controls, float oldDpi, float newDpi)
        {
            float scaleFactorChange = newDpi / oldDpi;

            foreach (Control control in controls)
            {
                control.Top = (int)(control.Top * scaleFactorChange);
                control.Left = (int)(control.Left * scaleFactorChange);
                control.Width = (int)(control.Width * scaleFactorChange);
                control.Height = (int)(control.Height * scaleFactorChange);
                control.Font = ScaleFont(control.Font, oldDpi, newDpi);
            }
        }

        private Font ScaleFont(Font font, float oldDpi, float newDpi)
        {
            float fontSizePx = 0.0f;
            float fontSizePt = 0.0f;

            fontSizePx = font.SizeInPoints / 72 * oldDpi;
            fontSizePt = fontSizePx * (newDpi / oldDpi) * 72 / oldDpi;

            return new Font(font.Name, fontSizePt, font.Style, GraphicsUnit.Point);
        }

        protected override void WndProc(ref Message m)
        {
            switch ((DPIHelper.WinMessages)m.Msg)
            {
                case DPIHelper.WinMessages.WM_DPICHANGED:
                    // Marshal the value in the lParam into a Rect.
                    RECT newDisplayRect = (RECT)Marshal.PtrToStructure(m.LParam, typeof(RECT));

                    // Remember current DPI and calculate current from WParam.
                    // Both X and Y are the same on Windows for Dpi.
                    m_oldDpi = m_newDpi;

                    m_newDpi.Width = (float)(m.WParam.ToInt32() >> 16);
                    m_newDpi.Height = (float)(m.WParam.ToInt32() & 0x0000FFFF);

                    // DPI should be the same for both width and height on Windows devices.
                    Debug.Assert(m_newDpi.Height == m_newDpi.Width);

                    if (m_oldDpi.Width != m_newDpi.Width)
                    {
                        OnDpiChangedEvent(newDisplayRect);
                    }
                    base.DefWndProc(ref m);
                    break;
                default:
                    base.WndProc(ref m);
                    break;
            }
        }
    }
}
```

<h3 id="custom-task-panes"><span data-ttu-id="aa092-280">Paneles de tareas personalizados</span><span class="sxs-lookup"><span data-stu-id="aa092-280">Custom task panes</span></span></h3>

<span data-ttu-id="aa092-281">Un panel de tareas personalizado se crea mediante Office como una ventana secundaria. </span><span class="sxs-lookup"><span data-stu-id="aa092-281">A custom task pane is created as a child window by Office.</span></span> <span data-ttu-id="aa092-282">Cuando se ejecuta en Windows Fall Creators Update (1709), el panel de tareas personalizado se ejecutará con el mismo modo de reconocimiento de PPP de Office.</span><span class="sxs-lookup"><span data-stu-id="aa092-282">When running on Windows Fall Creators Update (1709), your custom task pane will run using the same DPI awareness mode as Office.</span></span> <span data-ttu-id="aa092-283">Cuando se ejecuta en la actualización de abril 2018 de Windows (1803) y versiones posteriores, el panel de tareas personalizado se ejecutará con el modo de reconocimiento de PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="aa092-283">When running on Windows April 2018 Update (1803) and later, your custom task pane will run using System DPI awareness mode.</span></span> 

<span data-ttu-id="aa092-284">Como los paneles de tareas personalizados son ventanas secundarias, no pueden recibir notificaciones de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-284">Because custom task panes are child windows, they cannot receive DPI notifications.</span></span> <span data-ttu-id="aa092-285">Si se están dibujando correctamente, el usuario debe usar el [modo de compatibilidad de PPP de Office](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span><span class="sxs-lookup"><span data-stu-id="aa092-285">If they are drawing incorrectly, the user will need to use [Office DPI compatibility mode](https://support.office.com/en-us/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span></span>
<span data-ttu-id="aa092-286">Si el panel de tareas personalizado crea ventanas de nivel superior, esas ventanas pueden ejecutarse en cualquier modo de reconocimiento de PPP y recibir notificaciones de cambio de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-286">If your custom task pane creates top-level windows, those windows can run in any DPI awareness mode and receive DPI change notifications.</span></span> <span data-ttu-id="aa092-287">Para obtener más información, consulte la sección [Administración de la ventana de nivel superior](#top-level-window-management) de este artículo.</span><span class="sxs-lookup"><span data-stu-id="aa092-287">For more information, see the [Top-level window management](#top-level-window-management) section in this article.</span></span>

<h3 id="com-add-ins"><span data-ttu-id="aa092-288">Complementos COM</span><span class="sxs-lookup"><span data-stu-id="aa092-288">COM add-ins</span></span></h3>

<span data-ttu-id="aa092-289">Los complementos COM que crean ventanas de nivel superior pueden recibir notificaciones de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-289">COM add-ins that create top-level windows can receive DPI notifications.</span></span> <span data-ttu-id="aa092-290">Deberá crear un [bloque de contexto](#build-a-context-block-for-incoming-thread-calls) para establecer el subproceso al reconocimiento de PPP que quiera para la ventana y luego, deberá crear la ventana.</span><span class="sxs-lookup"><span data-stu-id="aa092-290">You should create a [context block](#build-a-context-block-for-incoming-thread-calls) to set the thread to the DPI awareness that you want for your window, then create your window.</span></span> <span data-ttu-id="aa092-291">Hay mucho que hacer para controlar las notificaciones de PPP correctamente, así que asegúrese de leer [Desarrollo de aplicaciones de escritorio de valores altos de PPP en Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="aa092-291">There’s a lot to handling the DPI notifications correctly, so be sure to read [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics) for more details.</span></span>

<span data-ttu-id="aa092-292">El mensaje [WM_DPICHANGED](https://docs.microsoft.com/windows/desktop/hidpi/wm-dpichanged) se envía un mensaje cuando se cambie el valor de PPP de una ventana.</span><span class="sxs-lookup"><span data-stu-id="aa092-292">The [WM_DPICHANGED](https://docs.microsoft.com/windows/desktop/hidpi/wm-dpichanged) message is sent when the DPI for a window has changed.</span></span>  <span data-ttu-id="aa092-293">En el código no administrado, este mensaje se controla mediante el [Procedimiento de ventana](https://docs.microsoft.com/windows/desktop/winmsg/using-window-procedures) para HWND.</span><span class="sxs-lookup"><span data-stu-id="aa092-293">In unmanaged code, this message is handled by the [Window Procedure](https://docs.microsoft.com/windows/desktop/winmsg/using-window-procedures) for the HWND.</span></span>  <span data-ttu-id="aa092-294">El código del controlador de cambios de PPP de ejemplo se encuentra en el artículo WM_DPICHANGED.</span><span class="sxs-lookup"><span data-stu-id="aa092-294">Sample DPI change handler code can be found in the WM_DPICHANGED article.</span></span> 

<span data-ttu-id="aa092-295">Los complementos COM que muestran las ventanas secundarias relacionadas con una ventana de Office no pueden recibir notificaciones de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-295">COM add-ins that show child windows that are parented to a window in Office cannot receive DPI notifications.</span></span> <span data-ttu-id="aa092-296">Si se están dibujando correctamente, el usuario debe usar el [modo de compatibilidad de PPP de Office](https://support.office.com/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span><span class="sxs-lookup"><span data-stu-id="aa092-296">If they are drawing incorrectly, the user will need to use [Office DPI compatibility mode](https://support.office.com/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span></span>

<h3 id="activex-controls"><span data-ttu-id="aa092-297">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="aa092-297">ActiveX controls</span></span></h3>

<span data-ttu-id="aa092-298">El modo de admitir el ajuste de PPP de controles ActiveX depende de si el control es con o sin ventana.</span><span class="sxs-lookup"><span data-stu-id="aa092-298">How to support DPI scaling in ActiveX controls depends on whether the control is windowed or windowless.</span></span>

#### <a name="windowed-activex-controls"></a><span data-ttu-id="aa092-299">Controles ActiveX con ventanas</span><span class="sxs-lookup"><span data-stu-id="aa092-299">Windowed ActiveX controls</span></span>

<span data-ttu-id="aa092-300">Los controles ActiveX con ventanas reciben un mensaje WM_SIZE cada vez que cambia de tamaño el control.</span><span class="sxs-lookup"><span data-stu-id="aa092-300">Windowed ActiveX controls receive a WM_SIZE message each time the control is resized.</span></span>  <span data-ttu-id="aa092-301">Cuando se desencadena el evento, el código del controlador de eventos puede llamar a la función [GetDpiForWindow](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) con HWND del control para obtener el valor de PPP, calcular las diferencias de factor de escala y ajustar según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="aa092-301">When this event is triggered, the event handler code can call the [GetDpiForWindow](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) function using the HWND of the control to get the DPI, calculate the scale factor differences, and adjust as needed.</span></span> 

<span data-ttu-id="aa092-302">El ejemplo siguiente permite a un control ActiveX basado en MFC responder al evento **OnSize**.</span><span class="sxs-lookup"><span data-stu-id="aa092-302">The following example enables an MFC-based ActiveX control to respond to the **OnSize** event.</span></span> 

```cpp
void ChangeWindowFontDPI(HWND hWnd, UINT dpi) 
{ 
LOGFONT fontInfo1 = { 0 }; 
// Calculate the font height based on the DPI. 
fontInfo1.lfHeight = -MulDiv(DESIRED_HEIGHT, dpi, 72); 
fontInfo1.lfQuality = CLEARTYPE_QUALITY; 
wcscpy_s(fontInfo1.lfFaceName, DESIRED_FONT_NAME); 
 
::SendMessage(hWnd, WM_SETFONT, (WPARAM)::CreateFontIndirectW(&fontInfo1), TRUE); 
} 
 
BOOL CALLBACK CMainDialog::EnumChildProc(HWND hWnd, LPARAM lParam) 
{ 
CMainDialog* _this = (CMainDialog*) lParam; 
if (_this != nullptr) 
{ 
// Calculate the scale factor difference between the old and new DPI changes. 
double scale = (((double) _this->m_newDPI) /  
   (((double) _this->m_currentDPI) / 100.0)) / 100; 
 
RECT rect = {}; 
::GetWindowRect(hWnd, &rect); 
 
POINT pt = { rect.left, rect.top }; 
::ScreenToClient(::GetParent(hWnd), &pt); 
 
// Adjust the window based on the scale changes. 
::MoveWindow(hWnd, 
pt.x * scale, 
pt.y * scale, 
(rect.right - rect.left) * scale, 
(rect.bottom - rect.top) * scale, 
TRUE); 
 
ChangeWindowFontDPI(hWnd, _this->m_newDPI); 
return TRUE; 
} 
return FALSE; 
} 
 
void CMainDialog::OnSize(UINT nType, int cx, int cy) 
{ 
CDialog::OnSize(nType, cx, cy); 
 
// Get the new DPI and enumerate the child windows that will use that value. 
m_currentDPI = ::GetDpiForWindow(this->GetSafeHwnd()); 
::EnumChildWindows(this->GetSafeHwnd(), EnumChildProc, (LPARAM)this); 
} 
```

#### <a name="windowless-activex-controls"></a><span data-ttu-id="aa092-303">Controles ActiveX sin ventanas</span><span class="sxs-lookup"><span data-stu-id="aa092-303">Windowless ActiveX controls</span></span>

<span data-ttu-id="aa092-304">No se garantiza que los controles ActiveX sin ventanas tengan un HWND.</span><span class="sxs-lookup"><span data-stu-id="aa092-304">Windowless ActiveX controls are not guaranteed have an HWND.</span></span>  <span data-ttu-id="aa092-305">Al insertar un control ActiveX en el lienzo de un documento, éste entrará en modo de diseño.</span><span class="sxs-lookup"><span data-stu-id="aa092-305">When an ActiveX control is inserted onto a document canvas, it is put into design mode.</span></span>  <span data-ttu-id="aa092-306">En las aplicaciones de Office, el contenedor host devolverá 0 para la llamada a hDC->GetWindow() en el evento ::OnDraw cuando el control está en modo de diseño.</span><span class="sxs-lookup"><span data-stu-id="aa092-306">In Office applications, the hosting container will return 0 for the call to hDC->GetWindow() in the ::OnDraw event when the control is in design mode.</span></span>  <span data-ttu-id="aa092-307">En este caso no se puede recuperar un valor de PPP confiable.</span><span class="sxs-lookup"><span data-stu-id="aa092-307">A reliable DPI cannot be retrieved in this case.</span></span> 

<span data-ttu-id="aa092-308">Sin embargo, cuando el control está en modo runtime, Office devolverá HWND donde se debe dibujar el control.</span><span class="sxs-lookup"><span data-stu-id="aa092-308">However, when the control is in runtime mode, Office will return the HWND where the control is to be drawn.</span></span>  <span data-ttu-id="aa092-309">En este caso, el desarrollador de control puede llamar a [GetDpiForWindow](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) y obtener el valor de PPP actual y las escalas de fuentes, los controles y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="aa092-309">In this case, the control developer can call [GetDpiForWindow](https://docs.microsoft.com/windows/desktop/api/winuser/nf-winuser-getdpiforwindow) and get the current DPI and scale fonts, controls, and so on.</span></span> 

<h3 id="ribbon-extensibility"><span data-ttu-id="aa092-310">Extensibilidad de la cinta de opciones personalizada</span><span class="sxs-lookup"><span data-stu-id="aa092-310">Custom ribbon extensibility</span></span></h3>

<span data-ttu-id="aa092-311">Todas las devoluciones de llamadas de Office para los controles de cinta de opciones personalizados se mostrarán en un reconocimiento de subprocesos de PPP del reconocimiento de PPP de sistema.</span><span class="sxs-lookup"><span data-stu-id="aa092-311">Any callbacks from Office for custom ribbon controls will be in a DPI thread awareness of System DPI aware.</span></span>  <span data-ttu-id="aa092-312">Si la solución se espera un reconocimiento de subprocesos de PPP diferente, deberá implementar un bloque de contexto para configurar el reconocimiento de subprocesos según lo esperado.</span><span class="sxs-lookup"><span data-stu-id="aa092-312">If your solution is expecting a different DPI thread awareness, you should implement a context block to set the thread awareness as expected.</span></span> <span data-ttu-id="aa092-313">Para obtener más información, vea [Crear un bloque de contexto](#build-a-context-block-for-incoming-thread-calls).</span><span class="sxs-lookup"><span data-stu-id="aa092-313">For more information, see [Build a context block](#build-a-context-block-for-incoming-thread-calls).</span></span>

<h3 id="ole"><span data-ttu-id="aa092-314">Clientes y servidores OLE.</span><span class="sxs-lookup"><span data-stu-id="aa092-314">OLE clients and servers</span></span></h3>

<span data-ttu-id="aa092-315">Cuando se hospeda un servidor OLE en un contenedor de cliente OLE, actualmente no puede proporcionar información de PPP actual o compatible.</span><span class="sxs-lookup"><span data-stu-id="aa092-315">When an OLE server is hosted within an OLE client container, you currently can’t provide current or supported DPI information.</span></span> <span data-ttu-id="aa092-316">Esto puede provocar problemas porque algunos modos mixtos de combinaciones de ventana principal y ventana secundaria no son compatibles con la arquitectura actual de Windows.</span><span class="sxs-lookup"><span data-stu-id="aa092-316">This can cause problems because some combinations of parent to child window mixed modes are not supported by the current Windows architecture.</span></span> <span data-ttu-id="aa092-317">Si Word o Excel detectan que hay varios monitores con escalas de PPP diferentes, no admitirán la activación en contexto.</span><span class="sxs-lookup"><span data-stu-id="aa092-317">If Word or Excel detect that there are multiple monitors with different DPI scales, they will not support in-place activation.</span></span> <span data-ttu-id="aa092-318">El servidor OLE se activará remotamente.</span><span class="sxs-lookup"><span data-stu-id="aa092-318">Your OLE server will activate out-of-place.</span></span> <span data-ttu-id="aa092-319">Si experimenta problemas con las interacciones de servidor OLE, el usuario deberá usar el [Modo de compatibilidad de PPP de Office](https://support.office.com/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span><span class="sxs-lookup"><span data-stu-id="aa092-319">If you are experiencing issues with OLE server interactions, the user will need to use [Office DPI compatibility mode](https://support.office.com/article/office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d).</span></span>

<h3 id="web-add-ins"><span data-ttu-id="aa092-320">Complementos web de Office</span><span class="sxs-lookup"><span data-stu-id="aa092-320">Office Web Add-ins</span></span></h3>

<span data-ttu-id="aa092-321">Los complementos de Office creados con la API de JavaScript de Office se ejecutan en un control de explorador.</span><span class="sxs-lookup"><span data-stu-id="aa092-321">Office Add-ins built using the Office JavaScript API run inside a browser control.</span></span> <span data-ttu-id="aa092-322">Puede controlar el ajuste de PPP con las mismas técnicas que se usan en cualquier diseño de aplicaciones web.</span><span class="sxs-lookup"><span data-stu-id="aa092-322">You can handle DPI scaling using the same techniques used in any web app design.</span></span> <span data-ttu-id="aa092-323">Muchos recursos en línea están disponibles para ayudarle a diseñar una página web para pantallas de alta resolución.</span><span class="sxs-lookup"><span data-stu-id="aa092-323">Many online resources are available to help design a web page for high resolution screens.</span></span>

## <a name="verify-that-your-solution-supports-dpi-scaling"></a><span data-ttu-id="aa092-324">Compruebe que la solución sea compatible con el ajuste de PPP</span><span class="sxs-lookup"><span data-stu-id="aa092-324">Verify that your solution supports DPI scaling</span></span>

<span data-ttu-id="aa092-325">Después de actualizar la aplicación para admitir el ajuste de PPP, debe validar los cambios en un entorno mixto de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-325">After you have updated your application to support DPI scaling, you should validate your changes in a mixed-DPI environment.</span></span> <span data-ttu-id="aa092-326">Valide que el código de la interfaz de usuario responda correctamente a los cambios de PPP, cuando se mueven las ventanas de su solución de una pantalla a otra con diferentes valores de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-326">Validate that your UI code responds properly to DPI changes when your solution’s windows are moved from one display to another that has different DPI values.</span></span> <span data-ttu-id="aa092-327">Para obtener más información sobre las técnicas de pruebas de ajuste de PPP, vea [Desarrollo de aplicaciones de escritorio con valores altos de PPP en Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).</span><span class="sxs-lookup"><span data-stu-id="aa092-327">For more information about DPI scaling testing techniques, see [High DPI Desktop Application Development on Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#related-topics).</span></span>

<span data-ttu-id="aa092-328">También pueden ser útiles estas técnicas adicionales:</span><span class="sxs-lookup"><span data-stu-id="aa092-328">You might also find these additional techniques helpful:</span></span>

- <span data-ttu-id="aa092-329">Con un equipo portátil, puede establecer el monitor principal a un monitor externo y luego, desacoplar el equipo portátil.</span><span class="sxs-lookup"><span data-stu-id="aa092-329">With a laptop, you can set the primary monitor to an external monitor, then undock the laptop.</span></span> <span data-ttu-id="aa092-330">Esto obligará el monitor principal a cambiar a la pantalla del equipo.</span><span class="sxs-lookup"><span data-stu-id="aa092-330">This will force the primary monitor to change to the laptop display.</span></span>
- <span data-ttu-id="aa092-331">Use la [herramienta WinSpy ++](https://github.com/BissetJ/winspy/releases) de código abierto para ayudar a depurar.</span><span class="sxs-lookup"><span data-stu-id="aa092-331">Use the open source [WinSpy++ tool](https://github.com/BissetJ/winspy/releases) to help debug.</span></span> <span data-ttu-id="aa092-332">Se puede usar para ver la configuración de reconocimiento de PPP de cualquier ventana.</span><span class="sxs-lookup"><span data-stu-id="aa092-332">You can use it to see the DPI awareness setting of any window.</span></span>
- <span data-ttu-id="aa092-333">Puede usar Escritorio remoto para probar varios monitores en un equipo remoto seleccionando Usar todos mis monitores para la sesión remota en la pestaña Pantalla, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="aa092-333">You can use remote desktop to test multiple monitors on a remote computer by selecting Use all my monitors for the remote session on the Display tab, as shown in the following screenshot.</span></span>

![Aplicación de una conexión a Escritorio remoto que muestra la pestaña Pantalla y selecciona Usar todos mis monitores para la sesión remota.](./media/remote-desktop-use-all-monitors.png)

## <a name="see-also"></a><span data-ttu-id="aa092-335">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa092-335">See also</span></span>

### <a name="articles"></a><span data-ttu-id="aa092-336">Artículos</span><span class="sxs-lookup"><span data-stu-id="aa092-336">Articles</span></span>

- <span data-ttu-id="aa092-337">[El desarrollo de una aplicación WPF con reconocimiento de PPP para cada monitor](https://docs.microsoft.com/windows/desktop/hidpi/declaring-managed-apps-dpi-aware) proporciona una guía general y una guía para escribir aplicaciones de escritorio de Win32.</span><span class="sxs-lookup"><span data-stu-id="aa092-337">[Developing a Per-Monitor DPI-Aware WPF Application](https://docs.microsoft.com/windows/desktop/hidpi/declaring-managed-apps-dpi-aware) provides a general overview and guide for writing Win32 desktop applications.</span></span> <span data-ttu-id="aa092-338">Muchas de las mismas técnicas descritas en este artículo se aplicarán a las soluciones de extensibilidad de Office.</span><span class="sxs-lookup"><span data-stu-id="aa092-338">Many of the same techniques described in this article will apply to Office extensibility solutions.</span></span>
- <span data-ttu-id="aa092-339">
  [API con reconocimiento PPP y ajuste de PPP de modo mixto](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-improvements-for-desktop-applications) cuenta con una lista de API relacionadas con PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-339">[Mixed-Mode DPI Scaling and DPI-aware APIs](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-improvements-for-desktop-applications) has a list of APIs related to DPI.</span></span>
- <span data-ttu-id="aa092-340">[Guía del desarrollador - PPP por monitor - Vista previa WPF](https://github.com/Microsoft/WPF-Samples/blob/master/PerMonitorDPI/Developer%20Guide%20-%20Per%20Monitor%20DPI%20-%20WPF%20Preview.docx) incluye la guía de desarrollo de aplicaciones WPF para crear aplicaciones WPF con reconocimiento de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-340">[Developer Guide - Per Monitor DPI - WPF Preview](https://github.com/Microsoft/WPF-Samples/blob/master/PerMonitorDPI/Developer%20Guide%20-%20Per%20Monitor%20DPI%20-%20WPF%20Preview.docx) covers the WPF app development guide for building DPI-aware WPF apps.</span></span>
- <span data-ttu-id="aa092-341">[Soporte técnico de Office para las pantallas de alta definición](https://support.office.com/article/Office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d) proporciona información sobre cómo un usuario puede configurar Office para optimizar la compatibilidad si la solución de Office no se admite correctamente cuando se cambie el valor de PPP.</span><span class="sxs-lookup"><span data-stu-id="aa092-341">[Office support for high definition displays](https://support.office.com/article/Office-support-for-high-definition-displays-6720ca0e-be59-41f6-b629-1369f549279d) provides information about how a user can set Office to optimize for compatibility if your Office solution is not supported properly when the DPI changes.</span></span>
- <span data-ttu-id="aa092-342">[Mostrar los cambios de escala de la Actualización de aniversario de Windows 10](https://blogs.technet.microsoft.com/askcore/2016/08/16/display-scaling-changes-for-the-windows-10-anniversary-update/) es una publicación de blog que trata los cambios en la actualización de aniversario de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="aa092-342">[Display Scaling changes for the Windows 10 Anniversary Update](https://blogs.technet.microsoft.com/askcore/2016/08/16/display-scaling-changes-for-the-windows-10-anniversary-update/) is a blog post that covers changes introduce with the Windows 10 Anniversary update.</span></span> 
- <span data-ttu-id="aa092-343">[Controlador DPI_AWARENESS_CONTEXT](https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context) contiene detalles de programación sobre definiciones y valores DPI_AWARENESS_CONTEXT.</span><span class="sxs-lookup"><span data-stu-id="aa092-343">[DPI_AWARENESS_CONTEXT handle](https://docs.microsoft.com/windows/desktop/hidpi/dpi-awareness-context) has programming details on the DPI_AWARENESS_CONTEXT values and definitions.</span></span>
- <span data-ttu-id="aa092-344">[Desarrollo de aplicaciones de escritorio con valores altos de PPP en Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#testing-your-changes) incluye información sobre las pruebas en la sección Probar los cambios.</span><span class="sxs-lookup"><span data-stu-id="aa092-344">[High DPI Desktop Application Development on Windows](https://docs.microsoft.com/windows/desktop/hidpi/high-dpi-desktop-application-development-on-windows#testing-your-changes) includes information about testing in the Testing Your Changes section.</span></span>

### <a name="code-samples"></a><span data-ttu-id="aa092-345">Ejemplos de código</span><span class="sxs-lookup"><span data-stu-id="aa092-345">Code samples</span></span>

- [<span data-ttu-id="aa092-346">Ejemplo de reconocimiento PPP por ventana</span><span class="sxs-lookup"><span data-stu-id="aa092-346">Per-window DPI Awareness sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DPIAwarenessPerWindow)
- [<span data-ttu-id="aa092-347">Ejemplo de PPP dinámico</span><span class="sxs-lookup"><span data-stu-id="aa092-347">Dynamic DPI sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DynamicDPI)
- [<span data-ttu-id="aa092-348">Ejemplo de WPF de reconocimiento por monitor</span><span class="sxs-lookup"><span data-stu-id="aa092-348">Per-Monitor Aware WPF sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)
