---
title: Connect (propiedad, RDS)
TOCTitle: Connect Property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb628356e4d93201c38cf84a9c3245b13e044ee3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486072"
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
    > <P>[!NOTA] Si especifica MS Remote como proveedor del objeto <STRONG>RDS.DataControl</STRONG>, se creará un escenario de cuatro niveles. No se han probado los escenarios de más de tres niveles y, en principio, no son necesarios.</P>



  - *DataControl*

  - Variable de objeto que representa un objeto **RDS.DataControl**.

