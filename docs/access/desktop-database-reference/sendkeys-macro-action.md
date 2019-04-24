---
title: EnviarTeclas (acción de macro)
TOCTitle: SendKeys macro action
ms:assetid: 3b06fcfc-ea64-c780-b5fc-6fc72853f524
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192656(v=office.15)
ms:contentKeyID: 48544275
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm183441
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f8c45cdf0d9cf588f61d1b51b728a8a15f6d7e12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308753"
---
# <a name="sendkeys-macro-action"></a>EnviarTeclas (acción de macro)

**Se aplica a:** Access 2013, Office 2013

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Nota de seguridad" alt="Security note" /><strong>Nota de seguridad</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Evite usar la instrucción <strong>SendKeys</strong> o una macro AutoKeys con información confidencial. Un usuario malintencionado podría interceptar las pulsaciones de tecla y poner en peligro la seguridad del equipo y sus datos.</td>
</tr>
</tbody>
</table>

Puede usar la acción **EnviarTeclas** para enviar pulsaciones de teclas directamente a Microsoft Access o a una aplicación activa basada en Windows.

> [!NOTE]
> [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **EnviarTeclas** utiliza los siguientes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de la acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Pulsaciones</strong></p></td>
<td><p>Las pulsaciones de teclas que van a ser procesadas por Access o por la aplicación. Introduzca las pulsaciones de teclas en el cuadro <strong>Pulsaciones de teclas</strong> de la sección <strong>Argumentos de acción</strong> del panel Generador de macros. Puede escribir hasta 255 caracteres. Este argumento es obligatorio.</p></td>
</tr>
<tr class="even">
<td><p><strong>Wait</strong></p></td>
<td><p>Especifica si la macro debe hacer una pausa hasta que las pulsaciones se hayan procesado. Haga clic en <strong>Sí</strong> para hacer una pausa, o en <strong>No</strong> para no hacerla. La opción predeterminada es <strong>No</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Access procesa las pulsaciones que recibe a través de la acción **EnviarTeclas** exactamente como si se hubieran escrito directamente en una ventana de Access.

Para especificar las pulsaciones, utilice la misma sintaxis que usaría para la instrucción **EnviarTeclas**.

> [!NOTE]
> Puede ocurrir un error si el argumento **Pulsaciones de teclas** contiene una sintaxis incorrecta, texto mal escrito u otros valores que no sean apropiados para la ventana a la que se envían las pulsaciones.

Puede usar esta acción para insertar información en un cuadro de diálogo, particularmente si no desea interrumpir la macro para responder de forma manual al cuadro de diálogo. Algunas acciones de Access, como **Imprimir** o **BuscarRegistro**, seleccionan de forma automática las opciones de determinados cuadros de diálogo de uso frecuente. Puede usar la acción **EnviarTeclas** para seleccionar las opciones de los cuadros de diálogo que se usan menos frecuentemente.

> [!NOTE]
> - Dado que el cuadro de diálogo suspende la macro, se deberá colocar la acción **EnviarTeclas** antes de la acción que abre el cuadro de diálogo, y establecer el argumento **Esperar** en **No**.
> - El momento en que las pulsaciones de teclas llegan a Access o a otra aplicación puede no ser el adecuado. Por ello, se recomienda que, si existe otro método (como la acción **BuscarRegistro** ) disponible para realizar la tarea deseada, se utilice en vez de usar la acción **EnviarTeclas** para rellenar las opciones de cuadros de diálogo.

Si desea enviar más de 255 caracteres a Access o a cualquier otra aplicación basada en Windows, puede utilizar varias acciones **EnviarTeclas** seguidas en una macro.

El uso de la acción **EnviarTeclas** para enviar pulsaciones de teclado desencadena los correspondientes eventos **KeyDown**, **KeyUp** y **KeyPress**. El envío de pulsaciones de teclas no ANSI (como una tecla de función) no desencadena el evento **KeyPress**.

Esta acción no está disponible en un módulo de Visual Basic para Aplicaciones (VBA). En su lugar, utilice la instrucción **EnviarTeclas**.

