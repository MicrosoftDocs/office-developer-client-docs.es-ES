---
title: Name (propiedad, ADOX)
TOCTitle: Name Property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 51ea68718c7605df03ed8e4d44d4cb48011649fd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483610"
---
# <a name="name-property-adox"></a><span data-ttu-id="d8724-102">Name (propiedad, ADOX)</span><span class="sxs-lookup"><span data-stu-id="d8724-102">Name Property (ADOX)</span></span>


<span data-ttu-id="d8724-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d8724-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d8724-104">Indica el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="d8724-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d8724-105">Configuraciones y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="d8724-105">Settings and Return Values</span></span>

<span data-ttu-id="d8724-106">Establece o devuelve un valor de tipo **String**.</span><span class="sxs-lookup"><span data-stu-id="d8724-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8724-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d8724-107">Remarks</span></span>

<span data-ttu-id="d8724-108">Los nombres no tienen por qué ser únicos dentro de una colección.</span><span class="sxs-lookup"><span data-stu-id="d8724-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="d8724-p101">La propiedad **Name** es de lectura y escritura en objetos [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md) y [User](user-object-adox.md). La propiedad **Name** es de sólo lectura en objetos [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md) y [View](view-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="d8724-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="d8724-111">Para objetos de lectura y escritura (objetos **Column**, **Group**, **Key**, **Index**, **Table** y **User**), el valor predeterminado es una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="d8724-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>


> [!NOTE]
> <P><span data-ttu-id="d8724-112">[!NOTA] Para claves, esta propiedad es de sólo lectura en objetos <STRONG>Key</STRONG> ya anexados a una colección.</span><span class="sxs-lookup"><span data-stu-id="d8724-112">For keys, this property is read-only on <STRONG>Key</STRONG> objects already appended to a collection.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="d8724-113">[!NOTA] Para tablas, esta propiedad es de sólo lectura en objetos <STRONG>Table</STRONG> ya anexados a una colección.</span><span class="sxs-lookup"><span data-stu-id="d8724-113">For tables, this property is read-only for <STRONG>Table</STRONG> objects already appended to a collection.</span></span></P>


