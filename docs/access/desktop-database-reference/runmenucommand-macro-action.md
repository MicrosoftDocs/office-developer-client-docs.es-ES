---
title: EjecutarComandoDeMenú (acción de macro)
TOCTitle: RunMenuCommand Macro Action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9d853c99fad322e17e8bbfd49cef27c14be33ffe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485226"
---
# <a name="runmenucommand-macro-action"></a>EjecutarComandoDeMenú (acción de macro)


**Se aplica a**: Access 2013 | Office 2013

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
> <P>[!NOTA] Al hacer clic en la pestaña <STRONG>Archivo</STRONG> y <STRONG>Reciente</STRONG>, se muestran las bases de datos utilizadas más recientemente. Puede hacer clic en una de estas bases de datos en lugar de hacer clic en <STRONG>Abrir</STRONG>. Estos elementos de base de datos no aparecen en el cuadro de lista desplegable para el argumento <STRONG>Comando</STRONG>, y no están disponibles cuando se utiliza la acción <STRONG>EjecutarComandoDeMenú</STRONG> en una macro.</P>



Cuando se convierte una base de datos de Access desde una versión anterior, es posible que algunos comandos dejen de estar disponibles. Puede que algún comando haya cambiado de nombre, se haya trasladado a un menú distinto o ya no esté disponible en Access. Las acciones **EjecutarComandoDeMenú** para tales comandos no pueden ser convertidas a acciones **EjecutarComandoDeMenú**. Cuando se abre la macro, Access muestra una acción **EjecutarComandoDeMenú** con un argumento **Comando** en blanco para esos comandos. Deberá modificar la macro y especificar un argumento de comando válido, o eliminar la acción **EjecutarComandoDeMenú**.

Para ejecutar la acción **EjecutarComandoDeMenú** en un módulo de Visual Basic para Aplicaciones (VBA), utilice el método **RunCommand** del objeto **Application** (equivalente al método **RunCommand** del objeto **DoCmd** ).

