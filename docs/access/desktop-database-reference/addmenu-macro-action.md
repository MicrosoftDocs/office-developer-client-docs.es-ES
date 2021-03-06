---
title: AgregarMenú (acción de macro)
TOCTitle: AddMenu macro action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 119e824cae71d54bb398aa68f476a667f14a6888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280276"
---
# <a name="addmenu-macro-action"></a>AgregarMenú (acción de macro)


**Se aplica a:** Access 2013, Office 2013

Este artículo describe la operación básica de la acción de macro **AgregarMenú**.

Puede usar la acción **AgregarMenú** para crear:

- Menús personalizados en la ficha **Complementos** para un formulario o informe particular.

- Un menú contextual personalizado para un formulario, un informe o un control. El menú contextual personalizado reemplaza el menú contextual integrado para el formulario, el informe o el control.

- Un menú contextual global. El menú contextual global reemplaza el menú contextual integrado para los campos en las hojas de datos de tabla y consulta, los formularios y los informes, excepto donde se agregó un menú contextual personalizado para un formulario, un informe o un control.

## <a name="setting"></a>Configuración

La acción **AgregarMenú** tiene los siguientes argumentos.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argumento de acción</p></th>
<th><p>Descripción</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Nombre del menú</strong></p></td>
<td><p>El nombre del menú, por ejemplo, &quot; Comandos de informe o Herramientas &quot; &quot; &quot; . Para crear una tecla de acceso para que pueda usar el teclado para elegir el menú, escriba una yand ( ) antes de la letra que desea que sea <strong>&amp;</strong> la clave de acceso. Esta letra se subrayará en el nombre del menú en la ficha <strong>Complementos</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Nombre de macro de menú</strong></p></td>
<td><p>El nombre del grupo de macros que contiene las macros para los comandos del menú. Es un argumento obligatorio. 

</p>
<p><strong>NOTA:</strong>Si ejecuta una macro que contiene la acción <strong>AgregarMenú</strong> en una base de datos de biblioteca, Microsoft Office Access 2007 busca el grupo de macros con este nombre solo en la base de datos actual.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Texto de la barra de estado</strong></p></td>
<td><p>El texto que se muestra en la barra de estado cuando se selecciona el menú. Este argumento se pasa por alto para los menús contextuales.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Comentarios

Para ejecutar la acción **AgregarMenú** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **AddMenu** del objeto **DoCmd**. También puede establecer la propiedad **MenuBar** o **ShortcutMenuBar** en VBA para crear un menú personalizado en la ficha **Complementos** o para asociar un menú contextual personalizado a un formulario, un informe o un control. Puede establecer la propiedad **ShortcutMenuBar** del objeto **Application** para crear un menú contextual global.

