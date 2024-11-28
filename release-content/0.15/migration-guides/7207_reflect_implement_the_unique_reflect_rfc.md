- Most instances of `dyn Reflect` should be changed to `dyn PartialReflect` which is less restrictive, however trait bounds should generally stay as `T: Reflect`.
- The new `PartialReflect::{as_partial_reflect, as_partial_reflect_mut, into_partial_reflect, try_as_reflect, try_as_reflect_mut, try_into_reflect}` methods as well as `Reflect::{as_reflect, as_reflect_mut, into_reflect}` will need to be implemented for manual implementors of `Reflect`.