---
title: AbrirMóduloVisualBasic (acción de macro)
TOCTitle: OpenVisualBasicModule macro action
ms:assetid: 26eb31c8-3c65-b17d-46cd-c8967434a7a0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191906(v=office.15)
ms:contentKeyID: 48543826
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm50916
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 55af2ce884b26b4c3df219e7d1986e7dc2e4c8ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288283"
---
# <a name="openvisualbasicmodule-macro-action"></a>AbrirMóduloVisualBasic (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Puede usar la acción **AbrirMóduloVisualBasic** para abrir un módulo especificado de Visual Basic para Aplicaciones (VBA) en un procedimiento especificado. Puede tratarse de un procedimiento Sub, un procedimiento de función o un procedimiento de evento.

> [!NOTE]
> Esta acción no se permitirá si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **AbrirMóduloVisualBasic** tiene los siguientes argumentos.

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
<td><p><strong>Nombre del módulo</strong></p></td>
<td><p>Nombre del módulo que se va a abrir. Deje este argumento en blanco si lo que desea es buscar un procedimiento en todos los módulos estándar de la base de datos y abrir el módulo que lo contenga en ese procedimiento. Si ejecuta una macro que contiene la acción <strong>AbrirMóduloVisualBasic</strong> en una base de datos de biblioteca, Microsoft Access primero buscar el módulo con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre del procedimiento</strong></p></td>
<td><p>Nombre del procedimiento en el que se desea abrir el módulo. Si deja en blanco este argumento, el módulo se abre en la sección Declaraciones.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Debe escribir un nombre válido en el argumento **Nombre del módulo** o **Nombre del procedimiento**.


## <a name="remarks"></a>Comentarios

Puede usar esta acción para abrir un procedimiento de evento especificando el argumento **nombre del módulo** y el argumento **nombre del procedimiento** . Por ejemplo, para abrir el procedimiento de evento **click** del botón imprimirfactura del formulario pedidos, establezca el argumento **nombre del módulo** en **formulario. pedidos** y establezca el argumento **nombre del procedimiento** en **\_imprimirfactura haga clic**en. Para ver un procedimiento de evento de un formulario o informe, éste debe estar abierto.

De forma similar, para abrir un procedimiento en un módulo de clase, debe especificar el nombre del módulo, si bien el módulo de clase no tiene que estar abierto.

Para abrir un procedimiento privado, el módulo que lo contiene debe estar abierto.

Esta acción tiene el mismo efecto que hacer clic con el botón secundario en un módulo en el panel de navegación y, a continuación, hacer clic en **Vista Diseño**. Esta acción también permite especificar un nombre de procedimiento y buscar procedimientos en los módulos estándar de una base de datos.

> [!TIP]
> [!SUGERENCIA] Puede seleccionar un módulo en el panel de navegación y arrastrarlo hasta una fila de acción de una macro. De esta forma, se crea automáticamente una acción **AbrirMóduloVisualBasic** que abre el módulo en la sección Declaraciones.

Para ejecutar la acción **AbrirMóduloVisualBasic** en un módulo de VBA, use el método **OpenModule** del objeto **DoCmd**.

