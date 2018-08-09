---
title: Acceso al código XLL en Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- acceso al código xll [excel 2007], XLL [Excel 2007], obtener acceso a código, comandos [Excel 2007], registro, funciones [Excel 2007], registro, llamar a los XLL de Excel, registrar comandos [Excel 2007], registrar funciones [Excel 2007]
localization_priority: Normal
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: 'Hace referencia a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1523f9e8213cb955f1bfd995c42f921b001299fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815522"
---
# <a name="accessing-xll-code-in-excel"></a>Acceso al código XLL en Excel

**Hace referencia a**: Excel 2013 | Office 2013 | Visual Studio 
  
Para ser accesibles en Microsoft Excel, las funciones y los comandos que contiene un XLL:
  
- Debe ser exportada por el XLL.
    
- Debe estar registrada con Excel.
    
## <a name="registering-functions-and-commands-with-excel"></a>Registrar las funciones y comandos con Excel

Registro indica a Excel lo siguiente acerca de un punto de entrada del archivo DLL:
  
- Si está oculto o, si una función, si está visible en el Asistente para la función.
    
- Si es que se puede llamar solo desde una hoja de macros XLM, o también desde una hoja de cálculo.
    
- Si un comando, si es una función de hoja de cálculo o una función equivalente de hoja de macro.
    
- ¿Cuál es su nombre de exportación DLL o XLL y qué nombre que desea que utilice Excel.
    
- Si se trata de una función:
    
  - ¿Qué datos tipos devuelve y toma como argumentos.
    
  - Si devuelve su resultado mediante la modificación de un argumento en su lugar.
    
  - Si es volátil.
    
  - Si es seguro para subprocesos (comenzando admitidos en Excel 2007).
    
  - ¿Qué editor de Autocompletar y el Asistente para la función pegar texto deben mostrar para ayudar con la función de llamada.
    
  - Qué función categoría debe aparecer en.
    
Todo esto se logra mediante la API C función [xlfRegister](xlfregister-form-1.md), equivalente a la función XLM **registrar**.
  
## <a name="calling-xll-functions-directly-from-excel"></a>Llamar a funciones XLL directamente desde Excel

Una vez registrados, funciones de hoja de hoja de cálculo y de macros XLL pueden llamarse desde cualquier lugar que una función integrada se puede llamar desde:
  
- Una sola celda o matriz fórmula en una hoja de cálculo.
    
- Una sola celda o matriz fórmula en una hoja de macros.
    
- La definición de un nombre definido.
    
- La condición y el límite de campos en un cuadro de diálogo Formato condicional.
    
- Desde otro complemento a través de la API de C funcionar [xlUDF](xludf.md).
    
- Desde Visual Basic para aplicaciones (VBA) a través del método **Application.Run** . 
    
Puede obtener una referencia a la celda o rango de celdas que llama dentro de la función mediante la función de API C **xlfCaller**. Si se llama a la función de la expresión de formato condicional de la celda, todavía se devuelve una referencia a la celda asociada o celdas, por lo que no se puede suponer que la fórmula de la celda contiene la función XLL. Si la función se ha llamado desde una función VBA definida por el usuario (UDF), **xlfCaller** vuelve a ser la dirección de las celdas que llamó a la función VBA. Para obtener más información, vea [xlfCaller](xlfcaller.md).
  
> [!NOTE]
> Excel también llama a código de función XLL desde los cuadros de diálogo **Asistente para la función Pegar** y **Reemplazar** . Es posible que necesite restringir el código ejecuta normal en el caso del cuadro de diálogo **Argumentos de la función Pegar** , especialmente donde la función puede tardar mucho tiempo en ejecutarse. Para detectar si desde cualquiera de estos cuadros de diálogo se llama a la función, debe implementar un fragmento de código en el proyecto que recorre en iteración todas las ventanas abiertas para determinar si la ventana en primer plano es uno de estos cuadros de diálogo y, si es así, cuál. 
  
## <a name="calling-xll-commands-directly-from-excel"></a>Llamar a los comandos XLL directamente desde Excel

Una vez registrados, pueden llamar a los comandos XLL en todas las formas en que se pueden llamar a otras macros definidas por el usuario:
  
- Por la que está asociada a un objeto de control incrustado en una hoja de cálculo.
    
- Desde el cuadro de diálogo Ejecutar Macro.
    
- Desde una macro VBA definida por el usuario mediante el método **Application.Run** . 
    
- Desde un elemento de menú personalizado o barra de herramientas.
    
- Mediante una pulsación de tecla de método abreviado configurar cuando se registra el comando.
    
- Como el comando se ejecute cuando se captura un evento especificado.
    
> [!NOTE]
> Comandos XLL están ocultos en que no aparecen en la lista de macros disponibles en los cuadros de diálogo de Excel. Pero se pueden especificar manualmente en el campo de nombre de macro. Excel espera que el nombre registrado como en estos cuadros de diálogo, no el nombre de la exportación del archivo DLL. 
  
Se supone que todos los comandos XLL registrados con Excel por Excel para tener el formato siguiente:
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

Excel omite el valor devuelto a menos que se le llame desde una hoja de macros XLM, en cuyo caso el valor devuelto se convierte a **TRUE** o **FALSE**. Por lo tanto, debe devolver 1 si el comando se ejecuta correctamente y 0 si tiene errores o el usuario lo cancela.
  
Puede obtener información acerca de cómo se ha invocado el comando se usa la API C función **xlfCaller**. Para obtener más información, vea [xlfCaller](xlfcaller.md).
  
Iniciar en la interfaz de usuario de Excel 2007 es muy diferente de las versiones anteriores. Las funciones de la API de C que permiten la adición y eliminación de barras de menús personalizadas, los menús, submenús, elementos de menú, barras de herramientas personalizadas y los botones de la barra de herramientas que aún se admiten en la mayoría de los casos. Sin embargo, es posible que no siempre que el elemento se ha agregado un ofrecen de modo que los usuarios están familiarizados con. Es recomendable comprobar minuciosamente que aún es accesible a cualquier funcionalidad se ha agregado o implementar una personalización específicas de la versión. Inicio de la interfaz de usuario en Excel 2007 mejor personalizado mediante el uso de un módulo de código administrado que, a continuación, estar estrechamente acoplado a los comandos XLL.
  
## <a name="see-also"></a>Vea también

- [Crear XLL](creating-xlls.md)
- [Llamar a funciones XLL desde el Asistente para funciones o los cuadros de diálogo Reemplazar](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)
- [Administrador de complementos y funciones de la interfaz de XLL](add-in-manager-and-xll-interface-functions.md)
- [Desarrollo de XLL de Excel de 2013](developing-excel-xlls.md)



