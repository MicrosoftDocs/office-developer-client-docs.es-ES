---
title: Crear una plantilla de formulario con código mediante el modelo de objetos de InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates,form templates [InfoPath 2007], creating InfoPath 2003-compatible,InfoPath 2007, creating InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: c746aeb1-902c-440e-830b-5b9efad0ca04
description: Los procedimientos de este tema describen cómo crear una plantilla de formulario que funcione con el modelo de objetos compatible con InfoPath 2003.
ms.openlocfilehash: 0cea526c2d41674afc6fee152c3e0584e6b69564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815868"
---
# <a name="create-a-form-template-using-the-infopath-2003-object-model"></a>Crear una plantilla de formulario con código mediante el modelo de objetos de InfoPath 2003

Los procedimientos de este tema describen cómo crear una plantilla de formulario que funcione con el modelo de objetos compatible con InfoPath 2003.
  
> [!IMPORTANT]
> [!IMPORTANTE] Además de los procedimientos siguientes, también debe hacer clic en la pestaña **Archivo**, hacer clic en **Guardar como** y seleccionar **Formulario de plantilla de InfoPath 2003** en el cuadro **Guardar como tipo** para guardar la plantilla en el formato de archivo compatible con InfoPath 2003. Asimismo, para abrir plantillas de formulario compatibles con InfoPath 2003 creadas con InfoPath, todos los usuarios de InfoPath 2003 deben tener .NET Framework 2.0 (o una versión posterior) instalado en el equipo. 
  
### <a name="to-create-an-infopath-2003-compatible-form-template-in-infopath-with-visual-studio-tools-for-applications"></a>Para crear una plantilla de formulario compatible con InfoPath 2003 en InfoPath con Visual Studio Tools for Applications

1. Inicie InfoPath Designer.
    
2. Haga clic en la pestaña **Archivo** y, a continuación, haga clic en **Opciones de formulario**.
    
3. En la categoría **Compatibilidad**, seleccione **Formulario de editor de InfoPath 2003**.
    
4. En la categoría **Programación**, seleccione **C# (compatible con InfoPath 2003)** o **Visual Basic (compatible con InfoPath 2003)** en la lista desplegable **Lenguaje del código de la plantilla de formulario**. 
    
5. Haga clic en **Aceptar**.
    
6. Diseñar la plantilla de formulario y, a continuación, agregue controladores de eventos en Visual Studio 2012, tal como se describe en [Agregar un controlador de eventos con el modelo de objetos de InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).
    
## <a name="see-also"></a>Vea también



[Tutorial: Crear y depurar una plantilla de formulario básica mediante el modelo de objetos de InfoPath 2003](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)
  
[Crear plantillas de formulario con código mediante el modelo de objetos de InfoPath 2003](creating-form-templates-using-the-infopath-2003-object-model.md)

