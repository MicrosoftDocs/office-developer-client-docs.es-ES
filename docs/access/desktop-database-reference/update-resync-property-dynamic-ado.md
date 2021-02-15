---
title: Update Resync dynamic property (ADO)
TOCTitle: Update Resync dynamic property (ADO)
ms:assetid: 0af9cfd2-8042-65c9-cec6-77d2e7a88ad9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248842(v=office.15)
ms:contentKeyID: 48543166
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 653291ade258d602d7ec523dcac7e9fe51dd91fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308347"
---
# <a name="update-resync-dynamic-property-ado"></a>Update Resync dynamic property (ADO)


**Se aplica a:** Access 2013, Office 2013

Especifica si el método [UpdateBatch](updatebatch-method-ado.md) va seguido de una operación implícita del método [Resync](resync-method-ado.md) y, en ese caso, el ámbito de esa operación.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve uno o varios de los valores [de ADCPROP \_ UPDATERESYNC \_ ENUM.](adcprop-updateresync-enum.md)

## <a name="remarks"></a>Comentarios

Los valores de ADCPROP UPDATERESYNC ENUM pueden combinarse, excepto \_ para adResyncAll que ya representa la combinación del resto \_ de los valores.

La constante **adResyncConflicts** almacena los valores de resincronización como valores subyacentes, aunque no reemplaza los cambios pendientes.

**Update Resync** es una propiedad dinámica que se anexa a la colección [Properties](properties-collection-ado.md) del objeto [Recordset](recordset-object-ado.md) cuando la propiedad [CursorLocation](cursorlocation-property-ado.md) está establecida en **adUseClient**.

