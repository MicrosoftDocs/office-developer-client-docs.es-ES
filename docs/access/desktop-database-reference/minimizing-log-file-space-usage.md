---
title: Minimizar el uso de espacio de archivo de registro
TOCTitle: Minimizing Log File Space Usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 119e4bc607296d1a68aef6f85d44f15718940b42
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25866988"
---
# <a name="minimizing-log-file-space-usage"></a>Minimizar el uso de espacio de archivo de registro


**Se aplica a**: Access 2013, Office 2013

Un archivo de registro se puede llenar rápidamente y, de esta forma, detener el servidor, si hay mucha actividad en una base de datos de SQL Server. Si selecciona la opción **Truncar registro en punto de comprobación** del archivo de registro, puede ampliar significativamente la vida del archivo de registro de una base de datos.

**Para habilitar la opción Truncar registro en punto de comprobación de Microsoft SQL Server 6.5**

1.  Inicie Microsoft SQL Server Enterprise Manager, abra el árbol del servidor y, a continuación, el árbol de dispositivos de base de datos.

2.  Haga doble clic en el nombre de la base de datos en la que se habilitará esta característica.

3.  En la pestaña **Base de datos**, seleccione **Truncamiento**.

4.  En la pestaña **Opciones**, seleccione **Truncar registro en punto de comprobación** y, a continuación, haga clic en **Aceptar**.

**Para habilitar Truncar registro en punto de comprobación en Microsoft SQL Server 7.0**

1.  Inicie Microsoft SQL Server Enterprise Manager, abra el árbol del servidor y, a continuación, el árbol de dispositivos de base de datos.

2.  Haga clic con el botón secundario en el nombre de la base de datos para la que se habilitará esta característica y seleccione **Propiedades**.

3.  En la pestaña **Opciones**, seleccione **Truncar registro en punto de comprobación** y, a continuación, haga clic en **Aceptar**.

Para obtener más información acerca de la característica **Truncar en punto de comprobación**, vea la documentación de Microsoft SQL Server.

