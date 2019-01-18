---
title: Actualizar la propiedad dinámica Resync (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28702029"
---
# <a name="update-resync-dynamic-property-ado"></a>Actualizar la propiedad dinámica Resync (ADO)


**Se aplica a**: Access 2013, Office 2013

Especifica si el método [UpdateBatch](updatebatch-method-ado.md) es seguido por una operación implícita del método [Resync](resync-method-ado.md) y, si es así, el ámbito de esa operación.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve uno o varios de los [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) valores.

## <a name="remarks"></a>Observaciones

Los valores de ADCPROP\_UPDATERESYNC\_ENUM se puede combinar, excepto adResyncAll, que ya representa la combinación del resto de los valores.

La constante **adResyncConflicts** almacena los valores de resincronización como valores subyacentes, aunque no reemplaza los cambios pendientes.

**Update Resync** es una propiedad dinámica que se anexa a la colección [Properties](recordset-object-ado.md) del objeto [Recordset](properties-collection-ado.md) cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.

