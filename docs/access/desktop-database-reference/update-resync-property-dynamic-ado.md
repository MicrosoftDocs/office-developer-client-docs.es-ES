---
title: dinámica Update Resync (propiedad, ADO)
TOCTitle: Update Resync Property--Dynamic (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f4eea391e99202eeb075d73daa1034dff2042e49
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604424"
---
# <a name="update-resync-property--dynamic-ado"></a>dinámica Update Resync (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Especifica si el método [UpdateBatch](updatebatch-method-ado.md) es seguido por una operación implícita del método [Resync](resync-method-ado.md) y, si es así, el ámbito de esa operación.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
=======
## <a name="settings-and-return-values"></a>Configuración y valores devueltos
>>>>>>> master

Establece o devuelve uno o varios de los [ADCPROP\_UPDATERESYNC\_ENUM](adcprop-updateresync-enum.md) valores.

## <a name="remarks"></a>Comentarios

Los valores de ADCPROP\_UPDATERESYNC\_ENUM se puede combinar, excepto adResyncAll, que ya representa la combinación del resto de los valores.

La constante **adResyncConflicts** almacena los valores de resincronización como valores subyacentes, aunque no reemplaza los cambios pendientes.

**Update Resync** es una propiedad dinámica que se anexa a la colección [Properties](recordset-object-ado.md) del objeto [Recordset](properties-collection-ado.md) cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.

