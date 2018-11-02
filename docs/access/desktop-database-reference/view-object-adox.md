---
title: Objeto View (ADOX - referencia de escritorio de la base de datos de Access)
TOCTitle: View object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 97376361a9ea5dcd71e3f9ef918a8ec7f1ebb0c0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920763"
---
# <a name="view-object-adox"></a><span data-ttu-id="fbd35-102">View (objeto, ADOX)</span><span class="sxs-lookup"><span data-stu-id="fbd35-102">View object (ADOX)</span></span>


<span data-ttu-id="fbd35-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fbd35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fbd35-p101">Representa un conjunto filtrado de registros o una tabla virtual. Cuando se utiliza junto con el objeto [Command](command-object-ado.md) de ADO, se puede usar el objeto **View** para agregar, eliminar o modificar vistas.</span><span class="sxs-lookup"><span data-stu-id="fbd35-p101">Represents a filtered set of records or a virtual table. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **View** object can be used for adding, deleting, or modifying views.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbd35-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fbd35-106">Remarks</span></span>

<span data-ttu-id="fbd35-p102">Una vista es una tabla virtual creada desde otras tablas de base de datos o vistas. El objeto **View** permite crear una vista sin necesidad de conocer ni utilizar la sintaxis "CREATE VIEW" del proveedor.</span><span class="sxs-lookup"><span data-stu-id="fbd35-p102">A view is a virtual table, created from other database tables or views. The **View** object allows you to create a view without having to know or use the provider's "CREATE VIEW" syntax.</span></span>

<span data-ttu-id="fbd35-109">Con las propiedades de un objeto **View**, se puede:</span><span class="sxs-lookup"><span data-stu-id="fbd35-109">With the properties of a **View** object, you can:</span></span>

  - <span data-ttu-id="fbd35-110">Identificar la vista con la propiedad [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="fbd35-110">Identify the view with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="fbd35-111">Especificar el objeto **Command** de ADO que se puede utilizar para agregar, eliminar o modificar vistas con la propiedad [Command](command-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="fbd35-111">Specify the ADO **Command** object that can be used to add, delete, or modify views with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="fbd35-112">Devolver información de fecha con las propiedades [DateCreated](datecreated-property-adox.md) y [DateModified](datemodified-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="fbd35-112">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

