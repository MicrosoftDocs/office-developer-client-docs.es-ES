---
title: Función Count (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Devuelve el número de registros de una tabla o consulta.
ms.openlocfilehash: 300fcbfd2aa927dd19516355ae28eec2adadf521
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815343"
---
# <a name="count-function-access-custom-web-app"></a><span data-ttu-id="5bb4a-103">Función Count (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="5bb4a-103">Count function (Access custom web app)</span></span>

<span data-ttu-id="5bb4a-104">Devuelve el número de registros de una tabla o consulta.</span><span class="sxs-lookup"><span data-stu-id="5bb4a-104">Returns the number of records in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="5bb4a-p101">Microsoft ya no recomienda crear ni usar aplicaciones web de Access en SharePoint. Como alternativa, considere la posibilidad de usar [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para crear soluciones empresariales sin código para la Web y dispositivos móviles.</span><span class="sxs-lookup"><span data-stu-id="5bb4a-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5bb4a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5bb4a-107">Syntax</span></span>

<span data-ttu-id="5bb4a-108">**Recuento** (*Expresión*)</span><span class="sxs-lookup"><span data-stu-id="5bb4a-108">**Count** (*Expression*)</span></span> 
  
<span data-ttu-id="5bb4a-109">La función **Count** contiene el siguiente argumento.</span><span class="sxs-lookup"><span data-stu-id="5bb4a-109">The **Count** function contains the following argument.</span></span> 
  
|<span data-ttu-id="5bb4a-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="5bb4a-110">**Argument name**</span></span>|<span data-ttu-id="5bb4a-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5bb4a-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5bb4a-112">*Expresión*</span><span class="sxs-lookup"><span data-stu-id="5bb4a-112">*Expression*</span></span>  <br/> |<span data-ttu-id="5bb4a-113">Una expresión de cadena que identifica el campo que contiene los datos que desea count o una expresión que realiza un cálculo utilizando los datos en el campo.</span><span class="sxs-lookup"><span data-stu-id="5bb4a-113">A string expression identifying the field that contains the data you want to count or an expression that performs a calculation using the data in the field.</span></span> <span data-ttu-id="5bb4a-114">Operandos de *expresión* pueden incluir el nombre de un campo de tabla o una función (que puede ser intrínseca o definida por el usuario pero no otra SQL funciones de agregado).</span><span class="sxs-lookup"><span data-stu-id="5bb4a-114">Operands in  *Expression*  can include the name of a table field or function (which can be either intrinsic or user-defined but not other SQL aggregate functions).</span></span> <span data-ttu-id="5bb4a-115">Se pueden contar todo tipo de datos, incluido texto.</span><span class="sxs-lookup"><span data-stu-id="5bb4a-115">You can count any kind of data, including text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bb4a-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5bb4a-116">Remarks</span></span>

<span data-ttu-id="5bb4a-p103">Puede usar Count para contar el número de registros de una consulta base. Por ejemplo, puede usar Count para contar el número de pedidos enviados a una región o país determinado.</span><span class="sxs-lookup"><span data-stu-id="5bb4a-p103">You can use Count to count the number of records in an underlying query. For example, you could use Count to count the number of orders shipped to a particular country or region.</span></span>
  
<span data-ttu-id="5bb4a-119">**Recuento** (\*) devuelve el número de elementos de un grupo.</span><span class="sxs-lookup"><span data-stu-id="5bb4a-119">**Count** (\*) returns the number of items in a group.</span></span> <span data-ttu-id="5bb4a-120">Esto incluye valores NULL y duplicados.</span><span class="sxs-lookup"><span data-stu-id="5bb4a-120">This includes NULL values and duplicates.</span></span> 
  

