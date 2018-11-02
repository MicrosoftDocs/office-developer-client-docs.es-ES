---
title: Create (método, ADOX)
TOCTitle: Create method (ADOX)
ms:assetid: d4072ee7-a0b9-7780-7be0-1d64b42b437c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250060(v=office.15)
ms:contentKeyID: 48547924
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 01f45adaf5bdd15841be86bfea62cca58e21a9d9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925522"
---
# <a name="create-method-adox"></a>Create (método, ADOX)


**Se aplica a**: Access 2013, Office 2013


Crea un nuevo catálogo.

## <a name="syntax"></a>Sintaxis

*Catálogo*. Crear*ConnectString*

## <a name="parameters"></a>Parámetros

  - *ConnectString*

  - Un valor **String** que se utiliza para conectarse al origen de datos.

## <a name="remarks"></a>Comentarios

El método **Create** crea y abre una nueva [conexión](connection-object-ado.md) de ADO con el origen de datos especificado en *ConnectString*. Si se ejecuta correctamente, el nuevo objeto **Connection** se asigna a la propiedad [ActiveConnection](activeconnection-property-adox.md).

Si el proveedor no admite la creación de catálogos nuevos, se producirá un error.

