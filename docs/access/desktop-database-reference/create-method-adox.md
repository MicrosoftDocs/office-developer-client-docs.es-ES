---
title: Create (método, ADOX)
TOCTitle: Create Method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cffaa8fb924d2fd272300c77fc5a9c3dc0b239db
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486140"
---
# <a name="create-method-adox"></a>Create (método, ADOX)


**Se aplica a**: Access 2013 | Office 2013


Crea un nuevo catálogo.

## <a name="syntax"></a>Sintaxis

*Catálogo*. Crear*ConnectString*

## <a name="parameters"></a>Parámetros

  - *ConnectString*

  - Un valor **String** que se utiliza para conectarse al origen de datos.

## <a name="remarks"></a>Comentarios

El método **Create** crea y abre una nueva [conexión](connection-object-ado.md) de ADO con el origen de datos especificado en *ConnectString*. Si se ejecuta correctamente, el nuevo objeto **Connection** se asigna a la propiedad [ActiveConnection](activeconnection-property-adox.md).

Si el proveedor no admite la creación de catálogos nuevos, se producirá un error.

