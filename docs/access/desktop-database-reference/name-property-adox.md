---
title: Name (propiedad, ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c7021c6f97d1aaa9c82e65eab98a3259d6eb87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288654"
---
# <a name="name-property-adox"></a><span data-ttu-id="9e60c-102">Name (propiedad, ADOX)</span><span class="sxs-lookup"><span data-stu-id="9e60c-102">Name property (ADOX)</span></span>

<span data-ttu-id="9e60c-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e60c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9e60c-104">Indica el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="9e60c-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="9e60c-105">Valores de configuración y devueltos</span><span class="sxs-lookup"><span data-stu-id="9e60c-105">Settings and return values</span></span>

<span data-ttu-id="9e60c-106">Establece o devuelve un valor de tipo **String**.</span><span class="sxs-lookup"><span data-stu-id="9e60c-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e60c-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9e60c-107">Remarks</span></span>

<span data-ttu-id="9e60c-108">Los nombres no tienen por qué ser únicos dentro de una colección.</span><span class="sxs-lookup"><span data-stu-id="9e60c-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="9e60c-p101">La propiedad **Name** es de lectura y escritura en objetos [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md) y [User](user-object-adox.md). La propiedad **Name** es de sólo lectura en objetos [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md) y [View](view-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="9e60c-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="9e60c-111">Para objetos de lectura y escritura (objetos **Column**, **Group**, **Key**, **Index**, **Table** y **User**), el valor predeterminado es una cadena vacía ("").</span><span class="sxs-lookup"><span data-stu-id="9e60c-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>

> [!NOTE]
> - <span data-ttu-id="9e60c-112">Para claves, esta propiedad es de sólo lectura en objetos **Key** ya anexados a una colección.</span><span class="sxs-lookup"><span data-stu-id="9e60c-112">For keys, this property is read-only on **Key** objects already appended to a collection.</span></span>
> - <span data-ttu-id="9e60c-113">[!NOTA] Para tablas, esta propiedad es de sólo lectura en objetos **Table** ya anexados a una colección.</span><span class="sxs-lookup"><span data-stu-id="9e60c-113">For tables, this property is read-only for **Table** objects already appended to a collection.</span></span>


