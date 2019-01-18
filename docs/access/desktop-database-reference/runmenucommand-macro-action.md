---
title: EjecutarComandoDeMenú (acción de macro)
TOCTitle: RunMenuCommand macro action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c2b5a19b7a92fb68dfb774afeec5cd6ba456f38d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698165"
---
# <a name="runmenucommand-macro-action"></a>EjecutarComandoDeMenú (acción de macro)

**Se aplica a**: Access 2013, Office 2013

La acción **EjecutarComandoDeMenú** sirve para ejecutar un comando integrado de Microsoft Access.

## <a name="setting"></a>Configuración

La acción **EjecutarComandoDeMenú** usa el siguiente argumento de acción.

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
<td><p><strong>Command</strong></p></td>
<td><p>El nombre del comando que desee ejecutar. El cuadro <strong>Comando</strong> muestra los comandos integrados disponibles en Access, por orden alfabético. Este argumento es obligatorio.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentarios

Puede usar la acción **EjecutarComandoDeMenú** para ejecutar un comando de Access desde una barra de menús personalizada, una barra de menús global, un menú contextual personalizado o un menú contextual global.

La acción **EjecutarComandoDeMenú** se puede utilizar en una macro con expresiones condicionales para ejecutar un comando según ciertas condiciones.

> [!NOTE]
> [!NOTA] Al hacer clic en la pestaña **Archivo** y **Reciente**, se muestran las bases de datos utilizadas más recientemente. Puede hacer clic en una de estas bases de datos en lugar de hacer clic en **Abrir**. Estos elementos de base de datos no aparecen en el cuadro de lista desplegable para el argumento **Comando**, y no están disponibles cuando se utiliza la acción **EjecutarComandoDeMenú** en una macro.

Cuando se convierte una base de datos de Access desde una versión anterior, es posible que algunos comandos dejen de estar disponibles. Puede que algún comando haya cambiado de nombre, se haya trasladado a un menú distinto o ya no esté disponible en Access. Las acciones **EjecutarComandoDeMenú** para tales comandos no pueden ser convertidas a acciones **EjecutarComandoDeMenú**. Cuando se abre la macro, Access muestra una acción **EjecutarComandoDeMenú** con un argumento **Comando** en blanco para esos comandos. Deberá modificar la macro y especificar un argumento de comando válido, o eliminar la acción **EjecutarComandoDeMenú**.

Para ejecutar la acción **EjecutarComandoDeMenú** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **RunCommand** del objeto **Application** (equivalente al método **RunCommand** del objeto **DoCmd** ).

