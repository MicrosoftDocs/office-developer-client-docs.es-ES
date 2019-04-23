---
title: AbrirDiagrama (acción de macro)
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4273d6858ad98b723d66ba32fe3b9aa7c902d31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288360"
---
# <a name="opendiagram-macro-action"></a>AbrirDiagrama (acción de macro)

**Se aplica a:** Access 2013, Office 2013

En un proyecto de Access, puede usar la acción **AbrirDiagrama** para abrir un diagrama de base de datos en la vista Diseño.

> [!NOTE]
> [!NOTA] Esta acción no estará permitida si la base de datos no es de confianza. 

## <a name="setting"></a>Configuración

La acción **AbrirDiagrama** tiene el siguiente argumento.

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
<td><p><strong>Nombre de diagrama</strong></p></td>
<td><p>Nombre del diagrama de base de datos que se va a abrir. El cuadro <strong>Nombre de diagrama</strong>, en la sección <strong>Argumentos de acción</strong> del panel Generador de macros, muestra todos los diagramas de la base de datos activa. Éste es un argumento obligatorio. Si ejecuta una macro que contiene la acción <strong>AbrirDiagrama</strong> en una base de datos de biblioteca, Microsoft Access busca primero el diagrama con este nombre en la base de datos de biblioteca y, a continuación, en la base de datos activa.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Comentarios

Esta acción es similar a hacer doble clic en un diagrama de base de datos en el panel de navegación, o bien, a hacer clic con el botón secundario en el diagrama de base de datos en el panel de navegación y después en **Vista Diseño**.

> [!TIP]
> [!SUGERENCIA] Puede arrastrar un diagrama de base de datos desde el panel de navegación hasta una fila de acción de una macro. De este modo, se crea automáticamente una acción **AbrirDiagrama** que abre el diagrama de base de datos en la vista Diseño.

Para ejecutar la acción **AbrirDiagrama** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **OpenDiagram** del objeto **DoCmd**.

