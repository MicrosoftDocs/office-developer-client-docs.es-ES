---
title: DataMember (propiedad, ADO)
TOCTitle: DataMember Property (ADO)
ms:assetid: f89e1d42-7993-764b-4e8a-2f449903f792
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250263(v=office.15)
ms:contentKeyID: 48548787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a67864ab135c59f146a27f997d4b0df63865a50
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486717"
---
# <a name="datamember-property-ado"></a><span data-ttu-id="185c4-102">DataMember (propiedad, ADO)</span><span class="sxs-lookup"><span data-stu-id="185c4-102">DataMember Property (ADO)</span></span>

<span data-ttu-id="185c4-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="185c4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="185c4-104">Indica el nombre del miembro de datos que se va a recuperar del objeto al que hace referencia la propiedad [DataSource](datasource-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="185c4-104">Indicates the name of the data member that will be retrieved from the object referenced by the [DataSource](datasource-property-ado.md) property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="185c4-105">Configuración y valores devueltos</span><span class="sxs-lookup"><span data-stu-id="185c4-105">Settings and Return Values</span></span>

<span data-ttu-id="185c4-p101">Establece o devuelve un valor de tipo **String**. El nombre no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="185c4-p101">Sets or returns a **String** value. The name is not case sensitive.</span></span>

## <a name="remarks"></a><span data-ttu-id="185c4-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="185c4-108">Remarks</span></span>

<span data-ttu-id="185c4-p102">Esta propiedad se usa para crear controles enlazados a datos con el Entorno de datos. El Entorno de datos mantiene colecciones de datos (orígenes de datos) que contienen objetos con nombre (*miembros de datos*) que se representarán como un objeto [ Recordset](recordset-object-ado.md). \*\*</span><span class="sxs-lookup"><span data-stu-id="185c4-p102">This property is used to create data-bound controls with the Data Environment. The Data Environment maintains collections of data (data sources) containing named objects (*data members*) that will be represented as a [Recordset](recordset-object-ado.md) object *.*</span></span>

<span data-ttu-id="185c4-111">Las propiedades **DataMember** y **DataSource** deben utilizarse conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="185c4-111">The **DataMember** and **DataSource** properties must be used in conjunction.</span></span>

<span data-ttu-id="185c4-p103">La propiedad **DataMember** determina cuál de los objetos especificados por la propiedad **DataSource** se va a representar como un objeto **Recordset**. El objeto **Recordset** debe estar cerrado para que se pueda establecer esta propiedad. Se genera un error si no se establece la propiedad **DataMember** antes de establecerse la propiedad **DataSource**, o bien, si el objeto especificado en la propiedad **DataSource** no reconoce el nombre de **DataMember**.</span><span class="sxs-lookup"><span data-stu-id="185c4-p103">The **DataMember** property determines which object specified by the **DataSource** property will be represented as a **Recordset** object. The **Recordset** object must be closed before this property is set. An error is generated if the **DataMember** property isn't set before the **DataSource** property, or if the **DataMember** name isn't recognized by the object specified in the **DataSource** property.</span></span>

<span data-ttu-id="185c4-115">**Uso**</span><span class="sxs-lookup"><span data-stu-id="185c4-115">**Usage**</span></span>

```vb
    Dim rs as New ADODB.Recordset
    rs.DataMember = "Command"     'Name of the rowset to bind to
    Set rs.DataSource = myDE      'Name of the object containing an IRowset
```
