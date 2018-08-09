---
title: Combina los función (aplicación web personalizado de Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Devuelve la primera expresión que no es nula de una lista de argumentos.
ms.openlocfilehash: cfe6f59c22a89b2a6d211e5f05c2dbf275d8da11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815332"
---
# <a name="coalesce-function-access-custom-web-app"></a><span data-ttu-id="a0555-103">Combina los función (aplicación web personalizado de Access)</span><span class="sxs-lookup"><span data-stu-id="a0555-103">Coalesce function (Access custom web app)</span></span>

<span data-ttu-id="a0555-104">Devuelve la primera expresión que no es nula de una lista de argumentos.</span><span class="sxs-lookup"><span data-stu-id="a0555-104">Returns the first expression that is not NULL from a list of arguments.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a0555-p101">La característica de almacenamiento en la nube descrita en este artículo no es compatible con Office 2013 ni Office 2016 y puede provocar el siguiente error: >  *Estamos teniendo problemas con el servidor, por lo que ahora mismo no podemos agregar \< servicio \>. Inténtelo de nuevo más tarde.* > En el caso del almacenamiento en la nube para Office Online, Office para iOS y Office para Android, puede buscar en nuestro [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="a0555-p101">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.* > For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a0555-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0555-107">Syntax</span></span>

<span data-ttu-id="a0555-108">**Combina los** (*Valor*, [*valor*],..., [*valor*])</span><span class="sxs-lookup"><span data-stu-id="a0555-108">**Coalesce** (*Value*, [*Value*], …,[*Value*])</span></span> 
  
<span data-ttu-id="a0555-109">La función de **combinación** contiene los siguientes argumentos</span><span class="sxs-lookup"><span data-stu-id="a0555-109">The **Coalesce** function contains the following arguments</span></span> 
  
|<span data-ttu-id="a0555-110">**Nombre del argumento**</span><span class="sxs-lookup"><span data-stu-id="a0555-110">**Argument name**</span></span>|<span data-ttu-id="a0555-111">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a0555-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a0555-112">*Value*</span><span class="sxs-lookup"><span data-stu-id="a0555-112">*Value*</span></span>  <br/> |<span data-ttu-id="a0555-113">Una expresión.</span><span class="sxs-lookup"><span data-stu-id="a0555-113">An expression.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0555-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a0555-114">Remarks</span></span>

<span data-ttu-id="a0555-115">Si todos los argumentos son NULL, **Coalesce** devuelve NULL.</span><span class="sxs-lookup"><span data-stu-id="a0555-115">If all arguments are NULL, **Coalesce** returns NULL.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a0555-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a0555-116">Example</span></span>

<span data-ttu-id="a0555-117">La siguiente expresión se usa como la regla de validación para una tabla.</span><span class="sxs-lookup"><span data-stu-id="a0555-117">The following expression is used as the validation rule for a table.</span></span> <span data-ttu-id="a0555-118">La expresión se asegura de que las entradas se realizan en los campos nombre de la primera, última nombre, correo electrónico, teléfono móvil, trabajo teléfono, principal, y compañía telefónica antes de confirmar un registro.</span><span class="sxs-lookup"><span data-stu-id="a0555-118">The expression ensures that entries are made in the First Name, Last Name, Email, Mobile Phone, Work Phone, Home Phone, and Company fields before a record is committed.</span></span> <span data-ttu-id="a0555-119">Si cualquiera de los campos enumerados se deja en blanco, la función de **combinación** devuelve Null, lo que infringe la regla de validación.</span><span class="sxs-lookup"><span data-stu-id="a0555-119">If any of the listed fields are left blank, the **Coalesce** function returns Null, which violates the validation rule.</span></span> 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


