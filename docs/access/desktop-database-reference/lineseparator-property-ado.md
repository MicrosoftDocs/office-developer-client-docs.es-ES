---
title: Propiedad LineSeparator (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e941339ad1c8622d1c87ada848a44fa82a9ef2d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289952"
---
# <a name="lineseparator-property-ado"></a>Propiedad LineSeparator (ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el carácter binario que se utiliza como separador de línea en objetos de texto [Stream](stream-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo [LineSeparatorsEnum](lineseparatorsenum.md) que indica el carácter separador de línea utilizado en el objeto **Stream**. El valor predeterminado es **adCRLF**.

## <a name="remarks"></a>Comentarios

**LineSeparator** se utiliza para interpretar líneas al leer el contenido de un objeto de texto **Stream**. Las líneas se pueden omitir con el método [SkipLine](skipline-method-ado.md).

**LineSeparator** sólo se utiliza con objetos de texto **Stream** ([Type](type-property-ado-stream.md) es **adTypeText**). Esta propiedad se pasa por alto si **Type** es **adTypeBinary**.

