---
title: DetenerMacro (acción de macro)
TOCTitle: StopMacro macro action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe319e0f7a811d3bcd3b2fc18c4a3d951187fbe8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308501"
---
# <a name="stopmacro-macro-action"></a>DetenerMacro (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **StopMacro** para detener la macro que se está ejecutando actualmente.

## <a name="setting"></a>Configuración

La **acción StopMacro** no tiene argumentos.

## <a name="remarks"></a>Comentarios

Normalmente, esta acción se usa cuando una condición hace necesario detener la macro. Puede usar una expresión condicional en la fila de acción de la macro que contiene esta acción. Cuando la expresión se evalúa como **True** (–1), Microsoft Access detiene la macro.

Por ejemplo, puede crear una macro que abra un formulario que muestre los totales de pedidos diarios de la fecha especificada en un cuadro de diálogo personalizado. Puede usar una expresión condicional para asegurarse de que el control **Fecha** de pedido del cuadro de diálogo contiene una fecha válida. Si no lo hace, la acción **Cuadro de** mensajes puede mostrar un mensaje de error y la **acción StopMacro** puede detener la macro.

Si la macro ha usado las acciones **Eco** o **SetWarnings** para desactivar el eco o la presentación de mensajes del sistema, la acción **StopMacro** los vuelve a activar automáticamente.

Esta acción no está disponible en un módulo de Visual Basic para Aplicaciones (VBA).

## <a name="example"></a>Ejemplo

En la siguiente macro se muestra el uso de la acción **AlOcurrirError**. En este ejemplo, la acción **AlOcurrirError** especifica que Access ejecute una macro de tratamiento de errores personalizada denominada ErrorHandler cuando se produzca un error. Cuando se produce un error, se llama al submacro CatchErrors. Si el número de error es 2102, se muestra un mensaje específico y se detiene la ejecución de macros. De lo contrario, se muestra un mensaje que describe el error y la macro se pausa para que pueda realizar una solución de problemas adicional. Esta macro mostrará un cuadro de mensaje referente al objeto **ErrorDeMacro** para mostrar información sobre el error.

**Código de ejemplo proporcionado por** la [Referencia del programador de Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
