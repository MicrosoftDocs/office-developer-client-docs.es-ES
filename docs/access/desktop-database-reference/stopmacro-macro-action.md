---
title: DetenerMacro (acción de macro)
TOCTitle: StopMacro Macro Action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a918fd128456450c21b5a36e74b7266df661cb75
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485041"
---
# <a name="stopmacro-macro-action"></a>DetenerMacro (acción de macro)

**Se aplica a**: Access 2013 | Office 2013

Puede utilizar la acción **DetenerMacro** para detener la macro que se está ejecutando.

## <a name="setting"></a>Configuración

La acción **DetenerMacro** no tiene ningún argumento.

## <a name="remarks"></a>Comentarios

Esta acción se suele utilizar cuando una condición haga necesario detener la macro. Puede usar una expresión condicional en la fila de acción de la macro que contiene esta acción. Cuando la expresión se evalúa como **True** (-1), Microsoft Access detiene la macro.

Por ejemplo, podría crear una macro que se abre un formulario que muestra los totales de pedidos diarios para la fecha especificada en un cuadro de diálogo personalizado. Podría utilizar una expresión condicional para asegurarse de que el control de **Fecha de pedido** en el cuadro de diálogo contiene una fecha válida. Si no es así, la acción de **cuadro de mensaje** puede mostrar un mensaje de error y la acción **DetenerMacro** puede detener la macro.

Si la macro ha utilizado las acciones **eco** o **EstablecerAdvertencias** para desactivar el eco o la presentación de mensajes del sistema, la acción **DetenerMacro volverá** a activarlos automáticamente.

Esta acción no está disponible en un módulo de Visual Basic para Aplicaciones (VBA).

## <a name="example"></a>Ejemplo

En la siguiente macro se muestra el uso de la acción **AlOcurrirError**. En este ejemplo, la acción **AlOcurrirError** especifica que Access ejecute una macro de tratamiento de errores personalizada denominada ErrorHandler cuando se produzca un error. Cuando se produce un error, se llama la submacro CatchErrors. Si el número de error es 2102, se muestra un mensaje específico y se detiene la ejecución de la macro. De lo contrario, se muestra un mensaje que describe el error y se detiene la macro para que pueda realizar la resolución de problemas adicional. Esta macro mostrará un cuadro de mensaje referente al objeto **ErrorDeMacro** para mostrar información sobre el error.

**Código de ejemplo proporcionado por** la [referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    /* MACRO: mcrThrowErrors                                  */
    /* PURPOSE: Error handling using macros in Access 2010    */
    
    OnError
        Go to Macro Name
        Macro Name CatchErrors
    
    OpenForm 
        Form Name frmSamples
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    MessageBox 
        Message This message appears after the OpenForm action
        Beep Yes
        Type None
        Title
    
    
    /* SUBMACRO: CatchErrors                                   */
    
    SubMacro: CatchErrors
        If [MacroError].[Number]=2101 Then
            MessageBox
                Message Cannot find the specified form!
                Beep Yes
                Type Critical
                Title
            StopMacro
    
        Else
            MessageBox
                Message =[MacroErro].[Description]
                Beep Yes
                Type None
                Title Unhandled Error
    
            SingleStep
        End If
    
    End SubMacro
```
