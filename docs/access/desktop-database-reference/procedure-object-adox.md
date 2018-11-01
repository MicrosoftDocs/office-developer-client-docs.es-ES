---
title: Procedure (objeto) (ADOX)
TOCTitle: Procedure Object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: afc4eae76395e7a15573ad5343955b0ab46df3db
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883354"
---
# <a name="procedure-object-adox"></a><span data-ttu-id="e4900-102">Procedure (objeto) (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e4900-102">Procedure Object (ADOX)</span></span>


<span data-ttu-id="e4900-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4900-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4900-p101">Representa un procedimiento almacenado. Cuando se usa junto con el objeto [Command](command-object-ado.md) de ADO, se puede usar el objeto **Procedure** para agregar, eliminar o modificar procedimientos almacenados.</span><span class="sxs-lookup"><span data-stu-id="e4900-p101">Represents a stored procedure. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **Procedure** object can be used for adding, deleting, or modifying stored procedures.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4900-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e4900-106">Remarks</span></span>

<span data-ttu-id="e4900-107">El objeto **Procedure** permite crear un procedimiento almacenado sin necesidad de conocer ni utilizar la sintaxis "CREATE PROCEDURE" del proveedor.</span><span class="sxs-lookup"><span data-stu-id="e4900-107">The **Procedure** object allows you to create a stored procedure without having to know or use the provider's "CREATE PROCEDURE" syntax.</span></span>

<span data-ttu-id="e4900-108">Con las propiedades de un objeto **Procedure**, se puede:</span><span class="sxs-lookup"><span data-stu-id="e4900-108">With the properties of a **Procedure** object, you can:</span></span>

  - <span data-ttu-id="e4900-109">Identificar el procedimiento con la propiedad [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e4900-109">Identify the procedure with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="e4900-110">Especificar el objeto **Command** de ADO que se puede utilizar para crear o ejecutar el procedimiento con la propiedad [Command](command-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e4900-110">Specify the ADO **Command** object that can be used to create or execute the procedure with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="e4900-111">Devolver información de fecha con las propiedades [DateCreated](datecreated-property-adox.md) y [DateModified](datemodified-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="e4900-111">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

