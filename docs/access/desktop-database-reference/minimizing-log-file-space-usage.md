---
title: Minimización del uso del espacio del archivo de registro
TOCTitle: Minimizing log file space usage
ms:assetid: d527c313-35ad-c30e-6ea1-ddfeff1fe890
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250073(v=office.15)
ms:contentKeyID: 48547960
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: da4bf7c9c30d3b9b37e2835ddeeeab2b2ed8a2c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715280"
---
# <a name="minimizing-log-file-space-usage"></a>Minimización del uso del espacio del archivo de registro

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

