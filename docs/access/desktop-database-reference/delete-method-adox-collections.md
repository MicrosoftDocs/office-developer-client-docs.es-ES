---
title: Método Delete (colecciones de ADOX)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 893890e43725d8c667ee5f72b396d3ec8947f395
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949372"
---
# <a name="delete-method-adox-collections"></a>Método Delete (colecciones de ADOX)

**Se aplica a**: Access 2013, Office 2013

Quita un objeto de una colección.

## <a name="syntax"></a>Sintaxis

*Colección*. Eliminar*nombre*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Name* |Un valor **Variant** que especifica el nombre o la posición ordinal (índice) del objeto que se va a eliminar.|

## <a name="remarks"></a>Comentarios

Se producirá un error si el *nombre* no existe en la colección.

Para colecciones [Tables](tables-collection-adox.md) y [Users](users-collection-adox.md), se producirá un error si el proveedor no admite la eliminación de tablas o de usuarios, respectivamente. Para colecciones [Procedures](procedures-collection-adox.md) y [Views](views-collection-adox.md), se producirá un error en **Delete** si el proveedor no admite comandos persistentes.

