---
title: Propiedad TableDef.DateCreated (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be76ed7f9d358963ea58776327ddafbb66f9d367
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923143"
---
# <a name="tabledefdatecreated-property-dao"></a><span data-ttu-id="9b2f4-102">Propiedad TableDef.DateCreated (DAO)</span><span class="sxs-lookup"><span data-stu-id="9b2f4-102">TableDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="9b2f4-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9b2f4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9b2f4-p101">Devuelve la fecha y la hora en que se creó un objeto (únicamente áreas de trabajo de Microsoft). **Variant** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="9b2f4-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b2f4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b2f4-106">Syntax</span></span>

<span data-ttu-id="9b2f4-107">*expresión* . DateCreated</span><span class="sxs-lookup"><span data-stu-id="9b2f4-107">*expression* .DateCreated</span></span>

<span data-ttu-id="9b2f4-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="9b2f4-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b2f4-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b2f4-109">Remarks</span></span>

<span data-ttu-id="9b2f4-p102">**DateCreated** y **LastUpdated** devuelven la fecha y la hora en que se creó o actualizó por última vez el objeto. En un entorno multiusuario, los usuarios deben obtener estos valores directamente del servidor de archivos para evitar discrepancias en los valores de las propiedades DateCreated y LastUpdated.</span><span class="sxs-lookup"><span data-stu-id="9b2f4-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

