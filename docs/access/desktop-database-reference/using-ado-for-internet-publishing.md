---
title: Utilizar ADO para publicaciones en Internet
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1e2d939f8583fdfd98ed1ae8e51a5bbfe792e486
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486307"
---
# <a name="using-ado-for-internet-publishing"></a><span data-ttu-id="c92f6-102">Utilizar ADO para publicaciones en Internet</span><span class="sxs-lookup"><span data-stu-id="c92f6-102">Using ADO for Internet Publishing</span></span>


<span data-ttu-id="c92f6-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c92f6-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="c92f6-p101">[OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) muestra un ejemplo específico de cómo obtener acceso a datos heterogéneos con ADO. Si bien los ejemplos de esta sección son específicos del proveedor de publicaciones en Internet, los principios descritos deben ser similares en el caso de utilizar ADO con otros proveedores para obtener acceso a datos heterogéneos, como un proveedor para obtener acceso a un almacén de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="c92f6-p101">[The OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) shows a specific example of accessing heterogeneous data with ADO. While the examples in this section will be specific to using the Internet Publishing Provider, the principles demonstrated should be similar when using ADO with other providers to heterogeneous data, such as a provider to an e-mail store.</span></span>

## <a name="urls"></a><span data-ttu-id="c92f6-106">Localizadores URL</span><span class="sxs-lookup"><span data-stu-id="c92f6-106">URLs</span></span>

<span data-ttu-id="c92f6-p102">Se pueden usar Localizadores uniformes de recursos (URL) como alternativa a las cadenas de conexión y al texto de comando para especificar los orígenes de datos y la ubicación de los archivos y directorios. Se pueden utilizar localizadores URL con los objetos [Connection](connection-object-ado.md) y **Recordset** existentes así como con los objetos **Record** y **Stream**.</span><span class="sxs-lookup"><span data-stu-id="c92f6-p102">Uniform Resource Locators (URLs) can be used as an alternative to connection strings and command text to specify data sources and the location of files and directories. You can use URLs with the existing [Connection](connection-object-ado.md) and **Recordset** objects as well as with the **Record** and **Stream** objects.</span></span>

<span data-ttu-id="c92f6-109">Para obtener más información sobre el uso de los localizadores URL, vea [Direcciones URL absolutas y relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="c92f6-109">For more information about using URLs, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span>

## <a name="record-fields"></a><span data-ttu-id="c92f6-110">Campos de registro</span><span class="sxs-lookup"><span data-stu-id="c92f6-110">Record Fields</span></span>

<span data-ttu-id="c92f6-p103">La diferencia distintiva entre los datos heterogéneos y los datos homogéneos reside en que, en el primer caso, cada fila de datos o **registro** puede tener un conjunto diferente de columnas o **campos**. En el caso de los datos homogéneos, cada fila tiene el mismo conjunto de columnas. Para obtener más información sobre los campos específicos del proveedor de publicaciones en Internet, vea [Registros y campos proporcionados por el proveedor](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="c92f6-p103">The distinguishing difference between heterogeneous data and homogeneous data is that for the former, each row of data, or **Record**, can have a different set of columns, or **Fields**. For homogeneous data, each row has the same set of columns. For more information about the fields specific to the Internet Publishing Provider, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>

## <a name="appending-new-fields"></a><span data-ttu-id="c92f6-114">Anexar campos nuevos</span><span class="sxs-lookup"><span data-stu-id="c92f6-114">Appending New Fields</span></span>

<span data-ttu-id="c92f6-115">Se han mejorado varios objetos de ADO para que funcionen conjuntamente con los objetos **Record** y **Stream**.</span><span class="sxs-lookup"><span data-stu-id="c92f6-115">Several ADO objects have been enhanced to work in conjunction with **Record** and **Stream** objects.</span></span>

  - <span data-ttu-id="c92f6-116">El método [Append](fields-collection-ado.md) de la colección [Fields](append-method-ado.md), que crea y agrega un objeto [Field](field-object-ado.md) a la colección, también puede especificar el valor de **Field**.</span><span class="sxs-lookup"><span data-stu-id="c92f6-116">The [Fields](fields-collection-ado.md) collection [Append](append-method-ado.md) method, which creates and adds a [Field](field-object-ado.md) object to the collection, can also specify the value of the **Field**.</span></span>

  - <span data-ttu-id="c92f6-117">El método [Update](update-method-ado.md) finaliza la adición o la eliminación de campos de la colección.</span><span class="sxs-lookup"><span data-stu-id="c92f6-117">The [Update](update-method-ado.md) method finalizes the addition or deletion of fields to the collection.</span></span>

  - <span data-ttu-id="c92f6-118">Como método abreviado y una alternativa al método **Append**, se pueden crear campos asignando simplemente un valor a un campo sin definir o un campo anteriormente eliminado.</span><span class="sxs-lookup"><span data-stu-id="c92f6-118">As a shortcut and alternative to the **Append** method, you may create fields by simply assigning a value to an undefined or previously deleted field.</span></span>

