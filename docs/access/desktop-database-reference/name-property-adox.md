---
title: Name (propiedad, ADOX)
TOCTitle: Name Property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ea92fcca60d0c2877bf89359aac4532356a9874
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604053"
---
# <a name="name-property-adox"></a><span data-ttu-id="00dea-102">Name (propiedad, ADOX)</span><span class="sxs-lookup"><span data-stu-id="00dea-102">Name Property (ADOX)</span></span>


<span data-ttu-id="00dea-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="00dea-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="00dea-104">Indica el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="00dea-104">Indicates the name of the object.</span></span>

<span data-ttu-id="00dea-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="00dea-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="00dea-106">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="00dea-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="00dea-107">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="00dea-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="00dea-108">master</span><span class="sxs-lookup"><span data-stu-id="00dea-108">master</span></span>

<span data-ttu-id="00dea-109">Establece o devuelve un valor de tipo **String**.</span><span class="sxs-lookup"><span data-stu-id="00dea-109">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00dea-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="00dea-110">Remarks</span></span>

<span data-ttu-id="00dea-111">Los nombres no tienen por qué ser únicos dentro de una colección.</span><span class="sxs-lookup"><span data-stu-id="00dea-111">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="00dea-p101">La propiedad **Name** es de lectura y escritura en objetos [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md) y [User](user-object-adox.md). La propiedad **Name** es de sólo lectura en objetos [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md) y [View](view-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="00dea-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="00dea-114">Para objetos de lectura y escritura (objetos **Column**, **Group**, **Key**, **Index**, **Table** y **User**), el valor predeterminado es una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="00dea-114">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>


> [!NOTE]
> <P><span data-ttu-id="00dea-115">[!NOTA] Para claves, esta propiedad es de sólo lectura en objetos <STRONG>Key</STRONG> ya anexados a una colección.</span><span class="sxs-lookup"><span data-stu-id="00dea-115">For keys, this property is read-only on <STRONG>Key</STRONG> objects already appended to a collection.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="00dea-116">[!NOTA] Para tablas, esta propiedad es de sólo lectura en objetos <STRONG>Table</STRONG> ya anexados a una colección.</span><span class="sxs-lookup"><span data-stu-id="00dea-116">For tables, this property is read-only for <STRONG>Table</STRONG> objects already appended to a collection.</span></span></P>


