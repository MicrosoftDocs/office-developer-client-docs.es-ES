---
title: Obtener una vista previa y dePurar plantillas de formulario de InfoPath con código
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- previewing form templates [infopath 2007],debugging form templates [InfoPath 2007],form templates [InfoPath 2007], previewing,debugging [InfoPath 2007], managed-code form templates,form templates [InfoPath 2007], debugging,InfoPath 2007, debugging form templates,InfoPath 2007, previewing form templates
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: Microsoft InfoPath con Visual Studio 2012 permite la depuración ejecutando el código del formulario en modo de vista previa. Cuando comienza a depurar el código, el proyecto se compila e InfoPath muestra el formulario en la ventana de vista previa. Cuando se encuentra una línea de código en la que se ha establecido un punto de interrupción, el foco se desplaza al editor de código. Si se continúa después del punto de interrupción, el foco vuelve a la ventana de vista previa. La depuración se detiene al cerrar la ventana de vista previa.
ms.openlocfilehash: 8f9ff97fdd5b4b016d96129304fa6f994d7b4561
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405243"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a>Obtener una vista previa y dePurar plantillas de formulario de InfoPath con código

Microsoft InfoPath con Visual Studio 2012 permite la depuración ejecutando el código del formulario en modo de vista previa. Cuando comienza a depurar el código, el proyecto se compila e InfoPath muestra el formulario en la ventana de vista previa. Cuando se encuentra una línea de código en la que se ha establecido un punto de interrupción, el foco se desplaza al editor de código. Si se continúa después del punto de interrupción, el foco vuelve a la ventana de vista previa. La depuración se detiene al cerrar la ventana de vista previa.
  
También puede modificar las opciones de la plantilla de formulario para obtener la vista previa y depurar usando un rol de usuario específico, un archivo de datos de ejemplo o especificando el dominio en el que se publicará el formulario. 
  
> [!NOTE]
> [!NOTA] No es posible depurar plantillas de formulario después de implementarlas en tiempo de ejecución en Visual Studio 2012. Esto incluye las plantillas de formulario que son compatibles solo con InfoPath, así como las compatibles con InfoPath y el explorador web que usa InfoPath Forms Services. No obstante, es posible registrar los valores en un campo desde el código en tiempo de ejecución para facilitar la depuración de la lógica empresarial de una plantilla de formulario. Para obtener información acerca de cómo hacerlo, consulte [registrar valores en un campo para](how-to-log-values-to-a-field-for-debugging.md)la depuración. 
  
## <a name="debugging-in-preview-mode"></a>Depurar en modo de vista previa

### <a name="to-debug-an-infopath-project-in-preview-mode"></a>Depurar un proyecto de InfoPath en modo de vista previa

1. Cree o abra un proyecto de plantilla de formulario con código administrado de InfoPath en Visual Studio 2012.
    
2. Establezca uno o más puntos de interrupción en el código del formulario en el editor de código haciendo clic en la barra gris situada a la izquierda de la línea de código en la que desea insertar el punto de interrupción.
    
    Aparecerá un círculo rojo y la línea de código se resaltará para indicar que, en tiempo de ejecución, se hará una pausa al llegar a este punto en el código del formulario.
    
3. En el menú **Depurar**, haga clic en **Iniciar depuración** (o presione F5).
    
    El proyecto se compilará y se mostrará el formulario en la ventana de vista previa.
    
4. Interactúe con el formulario hasta que encuentre una línea de código que contenga un punto de interrupción.
    
    El foco volverá al editor de código.
    
5. En el menú **Depurar**, haga clic en **Continuar** o bien presione F5.
    
6. Cuando haya finalizado la depuración, cierre la ventana de vista previa, haga clic en **Detener depuración** en el menú **Depurar**.
    
> [!NOTE]
> Para depurar una plantilla de formulario con código administrado de InfoPath al utilizar un miembro del modelo de objetos que requiere plena confianza, debe configurar la plantilla de formulario como se describe en [vista previa y depurar plantillas de formulario que requieren plena confianza](how-to-preview-and-debug-form-templates-that-require-full-trust.md). 
  
## <a name="using-a-sample-data-file"></a>Usar un archivo de datos de ejemplo

De manera predeterminada, la depuración y la vista previa utilizan el archivo template.xml que se crea junto con el proyecto. Puede crear su propio archivo de datos y especificar si desea utilizarlo al obtener la vista previa o depurar mediante el procedimiento siguiente. 
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a>Para especificar un archivo de datos de ejemplo para usarlo durante la depuración o la vista previa en Visual Studio Tools for Applications

1. Para ver template.xml, abra la plantilla de formulario en el modo de edición.
    
2. Haga clic en la pestaña **Archivo**, haga clic en **Guardar**, haga clic en **Guardar plantilla de formulario como** y haga clic en **Archivos de origen**.
    
3. Guarde los archivos de plantilla de formulario en una carpeta y después abra el archivo template.xml en un editor de texto.
    
4. Cree y guarde un archivo con la misma estructura que template.xml con los datos de ejemplo que desea usar.
    
5. Haga clic en la ficha **Archivo** y, a continuación, en **Opciones de formulario** en la ficha **Información**. 
    
6. Haga clic en la categoría **Vista previa** del cuadro de diálogo **Opciones de formulario** y a continuación, bajo **Datos de ejemplo**, especifique el archivo de datos de ejemplo que creó en el cuadro **Ubicación de archivo**. 
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a>Especificar un rol de usuario para utilizarlo durante la depuración o la vista previa

Si el formulario con el que está trabajando tiene definidos roles de usuario, puede especificar uno de ellos para utilizarlo durante la depuración o la vista previa. Para obtener información sobre cómo definir roles de usuario, busque "rol de usuario" en la Ayuda de InfoPath.
  
> [!NOTE]
> [!NOTA] La opción de especificar un rol de usuario no está disponible si la configuración de compatibilidad de la plantilla de formulario está establecida en **Formulario de explorador web**. Los roles de usuario no se admiten en las plantillas de formulario que se abren en el explorador desde InfoPath Forms Services. 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a>Para especificar un rol de usuario para utilizarlo durante la depuración o la vista previa

1. Si está trabajando en Visual Studio 2012, cambie a InfoPath Designer.
    
2. Haga clic en la pestaña **Archivo** y a continuación haga clic en **Opciones de formulario** en la ficha **Información**. 
    
3. Haga clic en la categoría **Vista previa** del cuadro de diálogo **Opciones de formulario** y especifique el rol de usuario en el cuadro desplegable **Vista previa como**. 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a>Especificar un dominio para utilizarlo durante la depuración o la vista previa

Puede tener una vista previa de un formulario según se publicó en un dominio específico. Esta configuración se aplicará únicamente si el nivel de seguridad de la plantilla de formulario está establecido en **Dominio**.
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a>Para especificar un dominio para utilizarlo durante la depuración o la vista previa

1. Si está trabajando en Visual Studio 2012, cambie a InfoPath Designer.
    
2. Haga clic en la pestaña **Archivo** y a continuación haga clic en **Opciones de formulario** en la ficha **Información**. 
    
3. Haga clic en la categoría **Vista previa** del cuadro de diálogo **Opciones de formulario** y especifique el dominio que usará durante la vista previa y la depuración en el cuadro **Dominio**. 
    
4. Haga clic en la categoría **Seguridad y confianza** del cuadro de diálogo **Opciones de formulario**, desactive la casilla **Determinar automáticamente el nivel de seguridad** y después haga clic en **Dominio**.
    

