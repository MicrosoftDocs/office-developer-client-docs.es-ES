---
title: Connect (propiedad, RDS)
TOCTitle: Connect Property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 191ef13d4d3c73bfbee50d72720d7e450376dd23
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862922"
---
# <a name="connect-property-rds"></a>Connect (propiedad, RDS)


**Se aplica a**: Access 2013 | Office 2013

Indica el nombre de la base de datos desde la que se ejecutan las operaciones de consulta y actualización.

La propiedad **Connect** se puede establecer en tiempo de diseño en las etiquetas OBJECT del objeto [RDS.DataControl](datacontrol-object-rds.md), o bien en tiempo de ejecución en el código del scripting (por ejemplo, VBScript).

## <a name="syntax"></a>Sintaxis

Tiempo de diseño: \<PARAM NAME = "Conectar" valor = "ConnectionString"\>

Tiempo de ejecución: DataControl.Connect = "ConnectionString"

## <a name="parameters"></a>Parámetros

- *ConnectionString*

  - Cadena de conexión válida. Para obtener información más general sobre las cadenas de conexión, vea la propiedad [ConnectionString](connectionstring-property-ado.md) o vea la documentación de su proveedor.
    
    > [!NOTE]
    > [!NOTA] Si especifica MS Remote como proveedor del objeto **RDS.DataControl**, se creará un escenario de cuatro niveles. No se han probado los escenarios de más de tres niveles y, en principio, no son necesarios.

- *DataControl*

  - Variable de objeto que representa un objeto **RDS.DataControl**.

