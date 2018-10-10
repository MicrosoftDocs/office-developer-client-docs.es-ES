---
title: Proveedor de persistencia de Microsoft OLE DB (proveedor de servicios ADO)
TOCTitle: Microsoft OLE DB Persistence Provider (ADO Service Provider)
ms:assetid: 22e41769-36eb-5a88-05ed-870938657624
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249007(v=office.15)
ms:contentKeyID: 48543719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ee7f29fa12b7158f2886f908666fa485ddf291cd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484767"
---
# <a name="microsoft-ole-db-persistence-provider-ado-service-provider"></a><span data-ttu-id="e0c13-102">Proveedor de persistencia de Microsoft OLE DB (proveedor de servicios ADO)</span><span class="sxs-lookup"><span data-stu-id="e0c13-102">Microsoft OLE DB Persistence Provider (ADO Service Provider)</span></span>


<span data-ttu-id="e0c13-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e0c13-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="e0c13-p101">El Proveedor de persistencia de Microsoft OLE DB permite guardar un objeto [Recordset](recordset-object-ado.md) en un archivo y, posteriormente, restaurar dicho objeto **Recordset** desde el archivo. Se conserva la información del esquema, los datos y los cambios pendientes.</span><span class="sxs-lookup"><span data-stu-id="e0c13-p101">The Microsoft OLE DB Persistence Provider enables you to save a [Recordset](recordset-object-ado.md) object into a file, and later restore that **Recordset** object from the file. Schema information, data, and pending changes are preserved.</span></span>

<span data-ttu-id="e0c13-106">El objeto **Recordset** se puede guardar en formato de propietario Advanced Data Table Gram (ADTG) o en el formato abierto XML (Lenguaje de marcado extensible).</span><span class="sxs-lookup"><span data-stu-id="e0c13-106">You can save the **Recordset** in either the proprietary Advanced Data Table Gram (ADTG) format, or the open Extensible Markup Language (XML) format.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="e0c13-107">Palabra clave del proveedor</span><span class="sxs-lookup"><span data-stu-id="e0c13-107">Provider Keyword</span></span>

<span data-ttu-id="e0c13-108">Para llamar a este proveedor, especifique la siguiente palabra clave y el siguiente valor en la cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="e0c13-108">To invoke this provider, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSPersist" 
```

## <a name="errors"></a><span data-ttu-id="e0c13-109">Errores</span><span class="sxs-lookup"><span data-stu-id="e0c13-109">Errors</span></span>

<span data-ttu-id="e0c13-110">En la aplicación se pueden detectar los errores siguientes emitidos por este proveedor.</span><span class="sxs-lookup"><span data-stu-id="e0c13-110">The following errors issued by this provider can be detected in your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e0c13-111">Constante</span><span class="sxs-lookup"><span data-stu-id="e0c13-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="e0c13-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0c13-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e0c13-113">E_BADSTREAM</span><span class="sxs-lookup"><span data-stu-id="e0c13-113">E_BADSTREAM</span></span></p></td>
<td><p><span data-ttu-id="e0c13-114">El archivo abierto no tiene un formato válido (es decir, el formato no es ADTG ni XML).</span><span class="sxs-lookup"><span data-stu-id="e0c13-114">The file opened does not have a valid format (that is, the format is not ADTG or XML).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e0c13-115">E_CANTPERSISTROWSET</span><span class="sxs-lookup"><span data-stu-id="e0c13-115">E_CANTPERSISTROWSET</span></span></p></td>
<td><p><span data-ttu-id="e0c13-116">El objeto guardado <strong>Recordset</strong> tiene características que le impiden ser almacenado.</span><span class="sxs-lookup"><span data-stu-id="e0c13-116">The <strong>Recordset</strong> object saved has characteristics that prevent it from being stored.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e0c13-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e0c13-117">Remarks</span></span>

<span data-ttu-id="e0c13-118">El Proveedor de persistencia de Microsoft OLE DB no expone ninguna propiedad dinámica.</span><span class="sxs-lookup"><span data-stu-id="e0c13-118">The Microsoft OLE DB Persistence Provider exposes no dynamic properties.</span></span>

<span data-ttu-id="e0c13-119">De momento, solo los objetos **Recordset** jerárquicos con parámetros no pueden ser guardados.</span><span class="sxs-lookup"><span data-stu-id="e0c13-119">Currently, only parameterized hierarchical **Recordset** objects cannot be saved.</span></span>

<span data-ttu-id="e0c13-120">Para obtener más información acerca del almacenamiento persistente de objetos **Recordset**, vea [Persistencia de Recordset](more-about-recordset-persistence.md).</span><span class="sxs-lookup"><span data-stu-id="e0c13-120">For more information about persistently storing **Recordset** objects, see [Recordset Persistence](more-about-recordset-persistence.md).</span></span>

<span data-ttu-id="e0c13-121">Cuando se utiliza una secuencia para abrir un **objeto Recordset**, debería haber parámetros no especifiquen más el parámetro *Source* del método **Open** .</span><span class="sxs-lookup"><span data-stu-id="e0c13-121">When a stream is used to open a **Recordset**, there should be no parameters specified other than the *Source* parameter of the **Open** method.</span></span>

