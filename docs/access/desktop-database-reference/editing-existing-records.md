---
title: Editar registros existentes
TOCTitle: Editing existing records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37da1e888eaa4231c58155e6830477f853b4027f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944672"
---
# <a name="editing-existing-records"></a>Editar registros existentes


**Se aplica a**: Access 2013, Office 2013

Para editar registros existentes, vaya a la fila que desea modificar y cambie la propiedad **Valor** de los campos que desea cambiar. Para obtener más información sobre la propiedad **Valor** del objeto **Field**, vea el [Capítulo 3: Examinar datos](chapter-3-examining-data.md). Dependiendo del tipo de cursor, se utilizará **Update** o **UpdateBatch** para enviar los cambios de vuelta al origen de datos. Para obtener más información, vea el [Capítulo 5: Actualizar y almacenar datos.](chapter-5-updating-and-persisting-data.md).

Normalmente es más eficaz utilizar un procedimiento almacenado con un objeto de comando para realizar actualizaciones, así como para realizar otras operaciones, ya que un procedimiento almacenado no requiere la creación de un cursor. Para obtener más información acerca de cursores, vea el [Capítulo 8: Cursores y bloqueos](chapter-8-understanding-cursors-and-locks.md).

